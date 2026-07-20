# Get Crypto Intraday with Alpha Vantage

Retrieves crypto intraday data from Alpha Vantage.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Get Crypto Intraday](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `interval` | query | `string` | yes | Query parameter $key for CRYPTO_INTRADAY. |
| `market` | query | `string` | yes | Query parameter $key for CRYPTO_INTRADAY. |
| `outputsize` | query | `string` | no | Query parameter $key for CRYPTO_INTRADAY. |
| `symbol` | query | `string` | yes | Query parameter $key for CRYPTO_INTRADAY. |
