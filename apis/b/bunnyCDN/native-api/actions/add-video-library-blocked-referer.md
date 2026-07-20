# Add Video Library Blocked Referer with BunnyCDN

Adds a blocked referer to a BunnyCDN video library.

## Endpoint

- **Method:** `POST`
- **Path:** `/videolibrary/:id/addBlockedReferrer`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Add Video Library Blocked Referer](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny video library ID. |
| `Hostname` | body | `string` | yes | Hostname to add to the blocked referer list. |
