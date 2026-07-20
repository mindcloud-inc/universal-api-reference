# Import DNS Records with BunnyCDN

Imports DNS records into BunnyCDN DNS zones.

## Endpoint

- **Method:** `POST`
- **Path:** `/dnszone/:zoneId/import`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Import DNS Records](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zoneId` | path | `string` | yes | The Bunny DNS zone ID. |
