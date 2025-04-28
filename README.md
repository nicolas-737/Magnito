workflows:
  flutter-build:
    name: Flutter Build
    max_build_duration: 60
    instance_type: mac_m1  # Bisa ganti dengan instance yang kamu pilih
    scripts:
      - name: Install dependencies
        script: |
          flutter pub get
      - name: Build APK
        script: |
          flutter build apk --release
    artifacts:
      - build/app/outputs/flutter-apk/app-release.apk
