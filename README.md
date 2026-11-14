# MYRA AI 3.0 Full Project

Android Studio/Gradle Kotlin Compose project. GitHub Actions builds a debug APK artifact.

## Build on GitHub (not Termux)
1. Extract this ZIP locally; upload the **contents** into repository root so `app/`, `build.gradle.kts`, `settings.gradle.kts`, and `.github/` are at root.
2. GitHub → Actions → MYRA AI 3.0 Full APK → Run workflow.
3. Download artifact `MYRA-AI-3.0-APK`.

## Gemini
In app Settings save your Google AI Studio key. API call uses:
`https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash:generateContent`
with `x-goog-api-key`. Actual HTTP code and Google error message are surfaced. 404 can still happen if model ID/API access/key is wrong; no code can guarantee a third-party service never fails.

## Feature inventory and maturity
- Animated neon orb UI, Gemini chat/key settings, speech input via Android recognizer, Hindi Android TTS, app-launch shortcuts, feature panels.
- Foreground service shell and Accessibility service shell included. Android requires user to grant microphone/notification and manually enable Accessibility. Wake phrase “Hello Myra” continuously listening is **not yet implemented** (requires an actual wake-word engine/model and battery/privacy safeguards).
- Live camera interpretation, ElevenLabs network TTS, persistent memory, online search provider, multi-agent task engine, and reliable autonomous workflows are **extension points/panels, not complete implementations** in this ZIP. Do not present them as already working.
- This starter cannot promise zero bugs. Test GitHub Actions and install on device; permissions/API key/model/network affect runtime.
- Never put API keys in GitHub source or workflow. Save key in app Settings.
