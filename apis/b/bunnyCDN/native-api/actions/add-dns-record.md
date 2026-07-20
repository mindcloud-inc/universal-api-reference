# Add DNS Record with BunnyCDN

Creates a new DNS record in BunnyCDN.

## Endpoint

- **Method:** `PUT`
- **Path:** `/dnszone/:zoneId/records`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Add DNS Record](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zoneId` | path | `string` | yes | The Bunny DNS zone ID. |
| `Type` | body | `string` | yes | DNS record type enum value. |
| `Name` | body | `string` | yes | DNS record name. |
| `Value` | body | `string` | yes | DNS record value. |
