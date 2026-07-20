# Get Forward Rate with Oanda

Retrieves forward rates from Oanda by tenor.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/rates/forward.:ext`
- **Base URL:** `https://exchange-rates-api.oanda.com`
- **Official documentation:** [Get Forward Rate](https://exchange-rates-api.oanda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `base` | query | `string` | yes | Base currency code. |
| `ext` | path | `string` | yes | Response format. |
| `quote` | query | `string` | yes | Quote currency code. |
| `source_date` | query | `string` | no | Historical source date. |
| `tenor` | query | `string` | no | Forward tenor or comma-separated list of tenors. |
