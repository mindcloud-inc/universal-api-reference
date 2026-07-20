# Get Supported Forwards with Oanda

Retrieves supported forward tenors from Oanda.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/supported_forwards.:ext`
- **Base URL:** `https://exchange-rates-api.oanda.com`
- **Official documentation:** [Get Supported Forwards](https://exchange-rates-api.oanda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `base` | query | `string` | no | Base currency or comma-separated list. |
| `data_set` | query | `string` | no | Dataset code. |
| `ext` | path | `string` | yes | Response format. |
| `quote` | query | `string` | no | Quote currency or comma-separated list. |
