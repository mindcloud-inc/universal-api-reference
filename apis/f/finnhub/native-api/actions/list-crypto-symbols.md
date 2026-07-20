# List Crypto Symbols with Finnhub

Retrieves crypto symbols from Finnhub.

## Endpoint

- **Method:** `GET`
- **Path:** `/crypto/symbol`
- **Base URL:** `https://finnhub.io/api/v1`
- **Official documentation:** [List Crypto Symbols](https://finnhub.io/docs/api#crypto-symbols)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exchange` | query | `string` | yes | Crypto exchange code, such as binance. |
