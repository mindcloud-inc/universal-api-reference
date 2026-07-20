# Remove Custom Hostname with BunnyCDN

Removes a custom hostname from a BunnyCDN pull zone.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/pullzone/:id/removeHostname`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Remove Custom Hostname](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny pull zone ID. |
| `Hostname` | body | `string` | yes | The hostname that will be removed. |
