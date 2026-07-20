# List Stock Symbols with Finnhub

Retrieves stock symbols from Finnhub.

## Endpoint

- **Method:** `GET`
- **Path:** `/stock/symbol`
- **Base URL:** `https://finnhub.io/api/v1`
- **Official documentation:** [List Stock Symbols](https://finnhub.io/docs/api#stock-symbols)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exchange` | query | `string` | yes | Exchange code for supported stock symbols, such as US. |
| `mic` | query | `string` | no | Optional MIC code filter. |
| `securityType` | query | `string` | no | Optional security type filter using OpenFIGI security type values. |
| `currency` | query | `string` | no | Optional currency filter. |
