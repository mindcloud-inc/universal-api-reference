# Add Video Library Allowed Referer with BunnyCDN

Adds an allowed referer to a BunnyCDN video library.

## Endpoint

- **Method:** `POST`
- **Path:** `/videolibrary/:id/addAllowedReferrer`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Add Video Library Allowed Referer](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny video library ID. |
| `Hostname` | body | `string` | yes | Hostname to add to the allowed referer list. |
