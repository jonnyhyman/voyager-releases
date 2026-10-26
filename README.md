# Voyager releases

Release artifacts for [Voyager](https://github.com/jonnyhyman), a music
streaming app. **There is no source code here** — only what the app needs in
order to update itself.

Each release carries:

| file | what it is |
| --- | --- |
| `latest.json` | the manifest `tauri-plugin-updater` polls, with the version, the notes, and a signature |
| `Voyager.app.tar.gz` | the update itself: a gzipped `.app` bundle |
| `Voyager.app.tar.gz.sig` | its minisign signature, which the app verifies before unpacking anything |
| `Voyager_<version>_<arch>.dmg` | a first-time install, for people rather than for the updater |

The app checks
`https://github.com/jonnyhyman/voyager-releases/releases/latest/download/latest.json`
and will only install an archive whose signature matches the public key built
into it.
