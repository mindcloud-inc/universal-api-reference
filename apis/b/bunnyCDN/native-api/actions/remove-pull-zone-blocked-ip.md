# Remove Pull Zone Blocked IP with BunnyCDN

Removes a blocked IP from a BunnyCDN pull zone.

## Endpoint

- **Method:** `POST`
- **Path:** `/pullzone/:id/removeBlockedIp`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Remove Pull Zone Blocked IP](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny pull zone ID. |
| `BlockedIp` | body | `string` | yes | The blocked IP to remove. |
