# CA bundle for signature verification

`verify-bundle.pem` holds the two **public** Certum certificates the signed MSIs
chain to (Certum Trusted Network CA 2 and Certum Code Signing 2021 CA). The Pages
workflow verifies every MSI against it before publishing. It contains no private
keys. Replace it only if the certificate authority chain changes.
