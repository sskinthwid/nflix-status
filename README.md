# Nflix availability

This public repository contains availability metadata and its control page only. Application source and builds stay private.

Open [the control page](https://sskinthwid.github.io/nflix-status/) to prepare a change, then use the GitHub editor to paste and commit the generated JSON to `status.json`.

- Set `version` to `"0"` to pause installed apps. Local profiles and progress remain saved.
- Set it to a nonzero semantic version such as `"1.5.0"` to enable them again.
- `message` is the notice shown in the app.
- Apps check on opening, foregrounding and about every minute. GitHub caching or offline devices can delay changes; offline apps use their last known status.
- This does not install new IPAs or provide tamper-proof access control.

Never add catalogue credentials, tokens, viewing history, source ZIPs or IPA files here.

`notifications.json` is the public announcement feed. Generate it using the separate private C# Notification Studio tool, upload it here and commit. It supports in-app banners/cards and opt-in scheduled phone alerts. GitHub cannot push new messages to a closed app; users open Nflix to download campaigns. An empty feed cancels remaining campaigns when devices next check. Use unique campaign IDs for new broadcasts, and do not include personal data.
