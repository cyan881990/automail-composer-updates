# Auto Mail Composer updates

Public Windows client distribution for Auto Mail Composer.

[Download version 1.1.0](packages/AutoMailComposer-1.1.0.zip): extract the ZIP and run `Install.cmd`. Requires Python 3.11+ with Tkinter and Codex CLI signed in on Windows.

The app checks `stable.json` at startup and every six hours while idle. Packages are pinned to immutable Git commits and verified using SHA-256 before installation. New versions activate on the next launch; a startup failure restores the previous version. Network failures retain the installed version.

This repository contains only the distributable client and update metadata. The Python client is readable source. Backend source, credentials, customer records, login sessions and drafts are not published here.

Publication: upload a new versioned package first, then update stable.json with its immutable commit URL, byte size and SHA-256. Do not overwrite existing versions. HTTPS and repository ownership are the trust boundary; packages are not independently digitally signed.
