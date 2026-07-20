# Get Historical Usage with The Org

Retrieves historical API usage from The Org.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.1/usage/history`
- **Base URL:** `https://api.theorg.com`
- **Official documentation:** [Get Historical Usage](https://developers.theorg.com/api/endpoints/usage-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api` | query | `list` | yes | The The Org API family to inspect in usage history. Accepted values: `0`, `1`, `2`. |
| `from` | query | `string` | yes | Start date in YYYY-MM-DD format |
| `to` | query | `string` | yes | End date in YYYY-MM-DD format |
| `interval` | query | `list` | no | The aggregation interval for the returned stats. Accepted values: `0`, `1`. |
