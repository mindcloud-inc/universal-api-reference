# Remove Pull Zone Allowed Referer with BunnyCDN

Removes an allowed referer from a BunnyCDN pull zone.

## Endpoint

- **Method:** `POST`
- **Path:** `/pullzone/:id/removeAllowedReferrer`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Remove Pull Zone Allowed Referer](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny pull zone ID. |
| `Hostname` | body | `string` | yes | The hostname to remove from allowed referrers. |
