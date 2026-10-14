# marinaMoji downloads

Mirror of the signed Windows installers from
[marinaMoji/marinaMoji releases](https://github.com/marinaMoji/marinaMoji/releases),
served over GitHub Pages because the Microsoft Store requires a direct,
non-redirecting download URL (GitHub release URLs redirect).

Layout: `https://marinamoji.github.io/downloads/windows/<tag>/marinaMoji-<tag>-windows-<x86_64|arm64>.msi`

To publish a new version: run `node scripts/sign-windows-release.mjs <tag> --upload`
in marinaMoji/marinaMoji. After the signed MSIs are uploaded and verified it adds
the tag to `versions.txt` here (it can also be added by hand), and the push
deploys. The workflow downloads each listed release's MSIs and refuses to publish
unless they match the release's `SHA256SUMS` **and** carry a valid Authenticode
signature (verified with `osslsigncode` against `ca/verify-bundle.pem`, with a
trusted timestamp) from the project's signing certificate. Never remove or change
a tag the Store has already accepted.
