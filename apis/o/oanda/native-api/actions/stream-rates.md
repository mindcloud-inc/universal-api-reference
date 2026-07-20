# Stream Rates with Oanda

Streams live exchange rates from Oanda.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/rates/stream.:ext`
- **Base URL:** `https://exchange-rates-api.oanda.com`
- **Official documentation:** [Stream Rates](https://exchange-rates-api.oanda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `base` | query | `string` | yes | Base currency or comma-separated list. |
| `data_set` | query | `string` | no | Dataset code. |
| `ext` | path | `string` | yes | Response format. |
| `quote` | query | `string` | no | Quote currency or comma-separated list. |
| `tenor` | query | `string` | no | Forward tenor or comma-separated list of tenors. |
