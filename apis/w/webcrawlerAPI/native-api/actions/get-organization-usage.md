# Get Organization Usage with Webcrawler API

Retrieves organization usage statistics from Webcrawler API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/organization/usage`
- **Base URL:** `https://api.webcrawlerapi.com`
- **Official documentation:** [Get Organization Usage](https://webcrawlerapi.com/docs/api/organization/usage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | no | Start date in YYYY-MM-DD format. |
| `to` | query | `string` | no | End date in YYYY-MM-DD format. |
| `include_daily` | query | `boolean` | no | Include daily breakdown in the response. |
