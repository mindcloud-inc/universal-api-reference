# Check DNS Zone Availability with BunnyCDN

Checks DNS zone availability in BunnyCDN.

## Endpoint

- **Method:** `POST`
- **Path:** `/dnszone/checkavailability`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Check DNS Zone Availability](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | DNS zone name to check. |
