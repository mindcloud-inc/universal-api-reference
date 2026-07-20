# Get Order Book with Oanda

Retrieves order book snapshots from Oanda.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/instruments/:instrument/orderBook`
- **Base URL:** `https://exchange-rates-api.oanda.com`
- **Official documentation:** [Get Order Book](https://exchange-rates-api.oanda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | no | The time of the snapshot to fetch. |
| `instrument` | path | `string` | yes | Instrument name, for example EUR_USD. |
