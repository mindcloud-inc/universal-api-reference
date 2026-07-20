# Get Interest Rate with Brasil API

Retrieves an interest rate from Brasil API by symbol.

## Endpoint

- **Method:** `GET`
- **Path:** `/taxas/v1/{sigla}`
- **Base URL:** `https://brasilapi.com.br/api`
- **Official documentation:** [Get Interest Rate](https://brasilapi.com.br/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sigla` | path | `string` | yes | The interest rate symbol to look up. |
