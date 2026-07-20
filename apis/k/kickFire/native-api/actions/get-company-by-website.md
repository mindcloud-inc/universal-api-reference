# Get Company by Website with KickFire

Retrieves company firmographic data from KickFire by website.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/company`
- **Base URL:** `https://api.kickfire.com`
- **Official documentation:** [Get Company by Website](https://foundryco.com/developers/#ip-to-company-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `website` | query | `string` | yes | Website or domain to enrich, without protocol or path. |
