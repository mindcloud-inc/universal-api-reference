# Get DNS Record Scan Result with BunnyCDN

Retrieves DNS record scan results from BunnyCDN.

## Endpoint

- **Method:** `GET`
- **Path:** `/dnszone/:zoneId/records/scan`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Get DNS Record Scan Result](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zoneId` | path | `string` | yes | The Bunny DNS zone ID. |
