# Create Certificate with Paradym

Creates a certificate in Paradym.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/certificates`
- **Base URL:** `https://api.paradym.id/v1`
- **Official documentation:** [Create Certificate](https://paradym.id/reference#tag/certificates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issuerAlternativeNameUrl` | body | `string` | yes | Issuer alternative name URL for the certificate. |
| `countryName` | body | `string` | yes | Two-letter country code for the certificate subject. Maximum length: 2. |
| `keyType` | body | `string` | yes | Cryptographic key type for the certificate. Accepted values: `0`, `1`. |
| `type` | body | `string` | yes | Paradym certificate purpose. Accepted values: `0`, `1`. |
| `commonName` | body | `string` | no | Optional common name for the certificate subject. |
