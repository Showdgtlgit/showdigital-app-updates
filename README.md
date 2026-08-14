# Show Digital app updates

Compiled builds and update manifests for the two Show Digital desktop
apps. The application source lives in private repositories; only
released artifacts are published here.

| File | App |
|---|---|
| `admin.json` | Show Digital Admin |
| `associate.json` | Show Digital Associate |

Each manifest names the current version, the download URL of that
release's asset, and its SHA-256. The apps read these files directly and
verify the checksum before installing anything.

Builds are signed with a local identity, not an Apple Developer ID, so
macOS Gatekeeper will block them on any machine other than the ones they
were made for. They also expect a specific Dropbox account, relay
service, and folder layout. Outside that setup they do nothing useful.

This repository is public so the apps can check for updates without
carrying a credential that would eventually expire.
