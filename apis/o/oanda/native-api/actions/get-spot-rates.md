# Get Spot Rates with Oanda

Retrieves spot exchange rates from Oanda.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/rates/spot.:ext`
- **Base URL:** `https://exchange-rates-api.oanda.com`
- **Official documentation:** [Get Spot Rates](https://exchange-rates-api.oanda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `base` | query | `string` | yes | Base currency or comma-separated list. |
| `data_set` | query | `string` | no | Dataset code. |
| `date_time` | query | `string` | no | ISO 8601 timestamp. |
| `ext` | path | `string` | yes | Response format. |
| `interbank` | query | `string` | no | Interbank pricing multiplier. |
| `quote` | query | `string` | no | Quote currency or comma-separated list. |
| `source_date` | query | `string` | no | Historical source date. |
