# Update DNS Record with BunnyCDN

Updates an existing DNS record in BunnyCDN.

## Endpoint

- **Method:** `POST`
- **Path:** `/dnszone/:zoneId/records/:id`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Update DNS Record](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny DNS record ID. |
| `zoneId` | path | `string` | yes | The Bunny DNS zone ID. |
