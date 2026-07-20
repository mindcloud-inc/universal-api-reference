# Set Force SSL with BunnyCDN

Updates force SSL settings for a BunnyCDN pull zone.

## Endpoint

- **Method:** `POST`
- **Path:** `/pullzone/:id/setForceSSL`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Set Force SSL](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny pull zone ID. |
| `Hostname` | body | `string` | yes | The hostname that will be updated. |
| `ForceSSL` | body | `string` | yes | Whether to force SSL on the given hostname. |
