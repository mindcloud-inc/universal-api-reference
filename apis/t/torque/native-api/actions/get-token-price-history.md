# Get Token Price History with Torque

## Endpoint

- **Method:** `GET`
- **Path:** `/token-price-history`
- **Base URL:** `https://app.torque.fi/api`
- **Official documentation:** [Get Token Price History](https://docs.torque.fi/business/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | query | `string` | yes | — |
| `timeframe` | query | `list` | no | Accepted values: `0`, `1`, `2`, `3`. |
