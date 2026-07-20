# List Currencies with Oanda

Retrieves supported currency codes from Oanda.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/currencies.:ext`
- **Base URL:** `https://exchange-rates-api.oanda.com`
- **Official documentation:** [List Currencies](https://exchange-rates-api.oanda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data_set` | query | `string` | no | Dataset code to filter currencies. |
| `ext` | path | `string` | yes | Response format. |
