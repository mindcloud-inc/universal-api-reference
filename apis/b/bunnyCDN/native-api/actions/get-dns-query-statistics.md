# Get DNS Query Statistics with BunnyCDN

Retrieves DNS query statistics from BunnyCDN.

## Endpoint

- **Method:** `GET`
- **Path:** `/dnszone/:id/statistics`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Get DNS Query Statistics](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny DNS zone ID. |
