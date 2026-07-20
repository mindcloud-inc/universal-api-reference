# Get Rates with Oanda

Retrieves exchange rates from Oanda for one base currency.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/rates/:base.:ext`
- **Base URL:** `https://exchange-rates-api.oanda.com`
- **Official documentation:** [Get Rates](https://exchange-rates-api.oanda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `base` | path | `string` | yes | Base currency code. |
| `data_set` | query | `string` | no | Dataset code. |
| `date` | query | `string` | no | Historical date in YYYY-MM-DD. |
| `decimal_places` | query | `string` | no | Decimal precision or all. |
| `end` | query | `string` | no | End date in YYYY-MM-DD. |
| `ext` | path | `string` | yes | Response format. |
| `fields` | query | `string` | no | Comma-separated response fields. |
| `quote` | query | `string` | no | Quote currency or comma-separated list of quote currencies. |
| `start` | query | `string` | no | Start date in YYYY-MM-DD. |
