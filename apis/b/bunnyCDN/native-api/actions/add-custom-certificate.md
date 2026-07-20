# Add Custom Certificate with BunnyCDN

Adds a custom certificate to a BunnyCDN pull zone.

## Endpoint

- **Method:** `POST`
- **Path:** `/pullzone/:id/addCertificate`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Add Custom Certificate](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny pull zone ID. |
| `Hostname` | body | `string` | yes | Hostname to attach the custom certificate to. |
| `Certificate` | body | `string` | yes | Base64-encoded certificate content. |
| `CertificateKey` | body | `string` | yes | Base64-encoded private key content. |
