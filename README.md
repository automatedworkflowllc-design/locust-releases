# Locust releases

Installers and update metadata for the Locust desktop app. The app checks this
repository's latest release on launch and installs the update on quit.

Each release carries the Windows installer, its blockmap, and latest.yml,
which is what the updater reads. Builds are currently unsigned, so Windows
SmartScreen warns on first install; that is expected for a pre-release.
