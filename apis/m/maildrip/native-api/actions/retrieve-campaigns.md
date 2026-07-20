# Retrieve campaigns with Maildrip

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/campaigns`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Retrieve campaigns](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search term to filter by campaign name |
| `date` | query | `date` | no | Filter by creation date (ISO format) |
