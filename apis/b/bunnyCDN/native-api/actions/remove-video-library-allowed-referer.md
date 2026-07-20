# Remove Video Library Allowed Referer with BunnyCDN

Removes an allowed referer from a BunnyCDN video library.

## Endpoint

- **Method:** `POST`
- **Path:** `/videolibrary/:id/removeAllowedReferrer`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Remove Video Library Allowed Referer](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny video library ID. |
| `Hostname` | body | `string` | yes | The hostname to remove from allowed referrers. |
