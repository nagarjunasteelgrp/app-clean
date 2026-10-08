# Nagarjuna Steel mobile app

Flutter CRM with contacts, tasks, attendance, travel summaries, and offline location tracking.

Clean snapshot of `professional app` at source commit `4de80f1`. Fresh Git history; existing UI unchanged. Design mockups are not included.

## Setup

Install Flutter and platform tools (SDK settings: `.fvmrc`, `pubspec.yaml`), then run `flutter pub get`.

Replace `YOUR_GOOGLE_MAPS_API_KEY` locally with your restricted Maps keys in:
- `lib/constants/constants.dart`
- `android/app/src/main/AndroidManifest.xml`
- `ios/Runner/AppDelegate.swift`

Do not commit real keys. Maps functionality requires this configuration.

Run `flutter run`. To use a test backend:

```sh
flutter run --dart-define=API_BASE_URL=https://your-test-api.example/api/v1/
```

Default API: `https://nagarjuna-crm-backend-309427312636.asia-south1.run.app/api/v1/`. Select the intended environment before testing.

## Builds and verification

```sh
flutter analyze
flutter test
flutter build apk --debug
```

Release builds require the existing signing keystore and an ignored `android/key.properties` with `storeFile`, `storePassword`, `keyAlias`, and `keyPassword`. The store path resolves from `android/app`. Obtain these files from the authorized signing owner.

This transfer was checked for source parity and excluded credentials. A new Flutter analysis, test run, or APK build was not performed during the transfer.

Signing files, password notes, environment files, generated builds, deployment workflows, and old Git history are excluded. This upload does not deploy services or publish an app release.
