# Export DNS Zone with BunnyCDN

Retrieves a DNS zone export from BunnyCDN.

## Endpoint

- **Method:** `GET`
- **Path:** `/dnszone/:id/export`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Export DNS Zone](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny DNS zone ID. |
