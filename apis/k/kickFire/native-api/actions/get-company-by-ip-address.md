# Get Company by IP Address with KickFire

Retrieves company firmographic data from KickFire by IP address.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/company`
- **Base URL:** `https://api.kickfire.com`
- **Official documentation:** [Get Company by IP Address](https://foundryco.com/developers/#ip-to-company-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | query | `string` | yes | Public IPv4 address to enrich. |
