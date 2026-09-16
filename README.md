# lancible-updates

Public version-check manifest for the Lancible Android app.

The main Lancible repo is private, so the sideloaded APK can't poll its
GitHub Releases API directly (that would need an embedded token, which is
extractable from a decompiled APK). Instead, the app fetches
[`latest.json`](latest.json) here — no auth needed — and compares the
`android.version` field against its own version to decide whether to show
an "update available" banner.

Update `latest.json` after publishing a new Lancible Android release.
