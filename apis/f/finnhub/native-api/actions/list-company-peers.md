# List Company Peers with Finnhub

Retrieves company peers from Finnhub.

## Endpoint

- **Method:** `GET`
- **Path:** `/stock/peers`
- **Base URL:** `https://finnhub.io/api/v1`
- **Official documentation:** [List Company Peers](https://finnhub.io/docs/api#company-peers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | query | `string` | yes | Company symbol, such as AAPL. |
| `grouping` | query | `string` | no | Optional peer grouping: sector, industry, or subIndustry. |
