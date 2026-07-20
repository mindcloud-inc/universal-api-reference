# Add Pull Zone Allowed Referer with BunnyCDN

Adds an allowed referer to a BunnyCDN pull zone.

## Endpoint

- **Method:** `POST`
- **Path:** `/pullzone/:id/addAllowedReferrer`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Add Pull Zone Allowed Referer](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny pull zone ID. |
| `Hostname` | body | `string` | yes | Hostname to add to the allowed referer list. |
