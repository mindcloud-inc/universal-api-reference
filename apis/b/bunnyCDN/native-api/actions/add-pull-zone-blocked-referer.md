# Add Pull Zone Blocked Referer with BunnyCDN

Adds a blocked referer to a BunnyCDN pull zone.

## Endpoint

- **Method:** `POST`
- **Path:** `/pullzone/:id/addBlockedReferrer`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Add Pull Zone Blocked Referer](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny pull zone ID. |
| `Hostname` | body | `string` | yes | Hostname to add to the blocked referer list. |
