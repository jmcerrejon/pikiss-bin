# AGENTS

## Repository Upload Policy

This repository stores distributable binaries directly in GitHub.
Do not upload artifacts to temporary external file hosts.

## How to Publish a New Artifact

1. Place the file in the correct folder:
   - `games/` for game packages
   - `hoster/` for hoster-related packages
   - `others/` for miscellaneous packages
2. Keep naming consistent with existing files in the target folder.
3. Commit the file to `main` and push to `origin`.
4. Share both links:
   - GitHub file page (`blob` URL)
   - Direct download (`raw` URL)

## Git Command Example

Example for publishing `games/openra-dev-rpi-aarch64.deb`:

1. `git add games/openra-dev-rpi-aarch64.deb`
2. `git commit -m "Add openra-dev-rpi-aarch64.deb"`
3. `git push origin main`
4. `git rev-parse --short HEAD` (use this hash in your confirmation)

## Large File Guidance

- If the file type is already tracked with Git LFS in `.gitattributes`, keep using LFS.
- If not tracked with LFS and GitHub accepts the push, keep the current repo convention.
- If GitHub rejects the file because of size, add or update LFS tracking before retrying.

## Response Template

When confirming publication, provide:

- Commit hash
- Blob URL
- Raw URL
