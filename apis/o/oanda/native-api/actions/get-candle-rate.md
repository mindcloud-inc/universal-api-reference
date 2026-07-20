# Get Candle Rate with Oanda

Retrieves one daily candle rate from Oanda.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/rates/candle.:ext`
- **Base URL:** `https://exchange-rates-api.oanda.com`
- **Official documentation:** [Get Candle Rate](https://exchange-rates-api.oanda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `base` | query | `string` | yes | Base currency or comma-separated list. |
| `data_set` | query | `string` | no | Dataset code. |
| `date_time` | query | `string` | no | ISO 8601 timestamp on a 15-minute boundary. |
| `decimal_places` | query | `string` | no | Decimal precision or all. |
| `ext` | path | `string` | yes | Response format. |
| `fields` | query | `string` | no | Comma-separated response fields. |
| `interbank` | query | `string` | no | Interbank pricing multiplier. |
| `quote` | query | `string` | no | Quote currency or comma-separated list. |
| `source_date` | query | `string` | no | Historical source date. |
