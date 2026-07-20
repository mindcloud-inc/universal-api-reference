# Remove Certificate with BunnyCDN

Removes a certificate from a BunnyCDN pull zone.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/pullzone/:id/removeCertificate`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Remove Certificate](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny pull zone ID. |
| `Hostname` | body | `string` | yes | The hostname from which the certificate will be removed. |
