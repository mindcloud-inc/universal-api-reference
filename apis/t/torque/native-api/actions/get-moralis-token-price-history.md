# Get Moralis Token Price History with Torque

## Endpoint

- **Method:** `GET`
- **Path:** `/moralis/token-price-history`
- **Base URL:** `https://app.torque.fi/api`
- **Official documentation:** [Get Moralis Token Price History](https://docs.torque.fi/business/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | query | `string` | yes | Token symbol. Torque's live endpoint currently requires symbol for this route. |
| `chain` | query | `string` | no | — |
| `timeframe` | query | `list` | no | Accepted values: `0`, `1`, `2`, `3`. |
