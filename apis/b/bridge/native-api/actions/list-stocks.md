# List Stocks with Bridge

Retrieves stocks from Bridge.

## Endpoint

- **Method:** `GET`
- **Path:** `/aggregation/stocks`
- **Base URL:** `https://api.bridgeapi.io/v3`
- **Official documentation:** [List Stocks](https://docs.bridgeapi.io/reference/getstocks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userAccessToken` | body | `string` | yes | Bridge user access token returned by the Authorization token action. |
| `since` | query | `date` | no | Limit to stocks updated after the specified timestamp |
| `account_id` | query | `number` | no | Filter stocks by account |
