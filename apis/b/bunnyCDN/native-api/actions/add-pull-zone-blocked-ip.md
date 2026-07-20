# Add Pull Zone Blocked IP with BunnyCDN

Adds a blocked IP to a BunnyCDN pull zone.

## Endpoint

- **Method:** `POST`
- **Path:** `/pullzone/:id/addBlockedIp`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Add Pull Zone Blocked IP](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny pull zone ID. |
| `BlockedIp` | body | `string` | yes | IP address to add to the blocked list. |
