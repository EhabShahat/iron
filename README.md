# Iron & Chalk — AI Studio import source

`index.html` is a byte-for-byte copy of the current V6.0 Unified Release standalone app, not the older PWA/Android kit's index file. This folder contains app source only. It contains no user workout data, Firebase credentials, or backup export.

Import this folder as the root of a private GitHub repository in Google AI Studio Build mode. The documented import control is **Add files (+) → Import from GitHub**. The ZIP of this folder is for transfer to a repository; extract it before committing. Run `npm install` and `npm run build` for a local build check.

The imported app currently uses IndexedDB (`iron-chalk-v2-standalone`) for data. Its optional cloud panel uses Supabase. Firebase is **not** wired in yet. Use `AI_STUDIO_PROMPT.md` to request the migration; verify code and working data before relying on Firestore.

Before opening the app at a new URL, export JSON from the existing `file://` app's Progress screen. Data in the browser's IndexedDB is not included in this ZIP and will not follow the app to another origin. Keep the backup private; do not upload the backup into an AI prompt or source repository.
