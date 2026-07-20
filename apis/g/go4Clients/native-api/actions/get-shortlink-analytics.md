# Get Shortlink Analytics with Go4Clients

Retrieves shortlink campaign analytics from Go4Clients.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/analytics/shortlink/v1.0`
- **Base URL:** `https://cloud.go4clients.com:8580`
- **Official documentation:** [Get Shortlink Analytics](https://apidoc.go4clients.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uniqueCampaignID` | query | `string` | no | Campaign ID to filter analytics for one shortlink campaign. |
| `start` | query | `number` | no | Initial pagination offset. |
| `limit` | query | `number` | no | Page size, maximum 5000. |
