# Remove Pull Zone Blocked Referer with BunnyCDN

Removes a blocked referer from a BunnyCDN pull zone.

## Endpoint

- **Method:** `POST`
- **Path:** `/pullzone/:id/removeBlockedReferrer`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Remove Pull Zone Blocked Referer](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny pull zone ID. |
| `Hostname` | body | `string` | yes | The hostname to remove from blocked referrers. |
