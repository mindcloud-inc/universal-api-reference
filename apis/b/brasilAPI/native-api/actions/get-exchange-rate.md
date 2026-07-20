# Get Exchange Rate with Brasil API

Retrieves a BRL exchange rate from Brasil API by currency and date.

## Endpoint

- **Method:** `GET`
- **Path:** `/cambio/v1/cotacao/{moeda}/{data}`
- **Base URL:** `https://brasilapi.com.br/api`
- **Official documentation:** [Get Exchange Rate](https://brasilapi.com.br/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moeda` | path | `string` | yes | The target currency code to quote against BRL. |
| `data` | path | `string` | yes | The quote date in YYYY-MM-DD format. |
