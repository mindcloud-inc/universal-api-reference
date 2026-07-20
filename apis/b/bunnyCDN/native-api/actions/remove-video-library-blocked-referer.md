# Remove Video Library Blocked Referer with BunnyCDN

Removes a blocked referer from a BunnyCDN video library.

## Endpoint

- **Method:** `POST`
- **Path:** `/videolibrary/:id/removeBlockedReferrer`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Remove Video Library Blocked Referer](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny video library ID. |
| `Hostname` | body | `string` | yes | The hostname to remove from blocked referrers. |
