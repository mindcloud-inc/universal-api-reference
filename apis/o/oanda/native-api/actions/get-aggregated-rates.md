# Get Aggregated Rates with Oanda

Retrieves aggregated candle rates from Oanda.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/rates/aggregated.:ext`
- **Base URL:** `https://exchange-rates-api.oanda.com`
- **Official documentation:** [Get Aggregated Rates](https://exchange-rates-api.oanda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `base` | query | `string` | yes | Base currency or comma-separated list. |
| `data_set` | query | `string` | no | Dataset code. |
| `decimal_places` | query | `string` | no | Decimal precision or all. |
| `end_time` | query | `string` | yes | ISO 8601 end timestamp on a 15-minute boundary. |
| `ext` | path | `string` | yes | Response format. |
| `fields` | query | `string` | no | Comma-separated response fields. |
| `interbank` | query | `string` | no | Interbank pricing multiplier. |
| `quote` | query | `string` | no | Quote currency or comma-separated list. |
| `start_time` | query | `string` | yes | ISO 8601 start timestamp on a 15-minute boundary. |
