# Get Dataset with Oanda

Retrieves exchange-rate dataset details from Oanda.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/datasets/:data_set.:ext`
- **Base URL:** `https://exchange-rates-api.oanda.com`
- **Official documentation:** [Get Dataset](https://exchange-rates-api.oanda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data_set` | path | `string` | yes | Dataset code. |
| `ext` | path | `string` | yes | Response format. |
