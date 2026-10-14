# marinaMoji downloads

Mirror of the signed Windows installers from
[marinaMoji/marinaMoji releases](https://github.com/marinaMoji/marinaMoji/releases),
served over GitHub Pages because the Microsoft Store requires a direct,
non-redirecting download URL (GitHub release URLs redirect).

Layout: `https://marinamoji.github.io/downloads/windows/<tag>/marinaMoji-<tag>-windows-<x86_64|arm64>.msi`

To publish a new version: sign and upload the release assets as usual, add the
tag to `versions.txt`, and push. The workflow downloads each listed release's
MSIs, checks them against the release's `SHA256SUMS` and deploys. Never remove
or change a tag the Store has already accepted.
