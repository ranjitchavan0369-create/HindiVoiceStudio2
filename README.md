# Hindi Voice Studio — starter project

This is a starter Android app using Android's built-in TextToSpeech engine for Hindi speech. It does not yet connect to an online AI voice provider.

## Build an APK using only your Android phone

1. Download and extract this ZIP on your phone.
2. In your browser, sign in to GitHub and create a new repository named `HindiVoiceStudio`.
3. Upload the extracted project files and folders to the repository. Make sure `.github/workflows/build-apk.yml` is included. GitHub's web upload can be awkward for hidden folders; if it is missing, create the workflow file in the repository using the exact path `.github/workflows/build-apk.yml`.
4. Open the repository's **Actions** tab and enable workflows if prompted.
5. Select **Build Hindi Voice Studio APK**, press **Run workflow**, then open the completed run.
6. Under **Artifacts**, download `HindiVoiceStudio-debug-apk`. Extract the downloaded artifact ZIP to get `app-debug.apk`.
7. Tap the APK to install it. If Android asks, allow your browser or file manager to install unknown apps for this installation only. Install only APKs you built or trust.

GitHub Actions free usage has limits. A public repository normally avoids using private-repository build minutes for standard hosted runners, but GitHub policies can change. Do not upload API keys or private data to a public repository.

## Offline Hindi voice

The app uses the phone's installed Android Text-to-Speech engine. If Hindi is not available, open Settings and search for **Text-to-speech output** or **Speech Services by Google**, then install Hindi voice data. Exact menu names differ by phone.

## Current limitations

- This is a basic starter, not a polished production app.
- The Save Audio action creates a WAV file in app-specific music storage. A later version should add a proper Share/Export button and robust completion/error handling.
- AI voice mode is a placeholder. To add it safely, choose an AI TTS provider with a free tier and put credentials on a secure backend, not in the APK.
- Long text may exceed the speech engine's per-request limit; later we can split text into chunks.
- No warranty is made that the project builds on every future Android/Gradle environment.
