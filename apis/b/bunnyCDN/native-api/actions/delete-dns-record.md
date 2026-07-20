# Delete DNS Record with BunnyCDN

Deletes an existing DNS record from BunnyCDN.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/dnszone/:zoneId/records/:id`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Delete DNS Record](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny DNS record ID. |
| `zoneId` | path | `string` | yes | The Bunny DNS zone ID. |
