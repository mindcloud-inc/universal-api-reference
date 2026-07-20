# List Earnings Surprises with Finnhub

Retrieves earnings surprises from Finnhub.

## Endpoint

- **Method:** `GET`
- **Path:** `/stock/earnings`
- **Base URL:** `https://finnhub.io/api/v1`
- **Official documentation:** [List Earnings Surprises](https://finnhub.io/docs/api#company-earnings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | query | `string` | yes | Company symbol, such as AAPL. |
| `limit` | query | `number` | no | Optional number of earnings surprise records to return. |
