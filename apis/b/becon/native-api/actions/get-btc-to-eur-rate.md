# Get BTC to EUR Rate with Becon

Retrieves the BTC-to-EUR rate from Becon.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/currencies/:cryptoCurrencyName`
- **Base URL:** `https://external-api.bcon.global/api`
- **Official documentation:** [Get BTC to EUR Rate](https://bcon.global/integrations/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cryptoCurrencyName` | path | `string` | yes | The cryptocurrency code in the path, such as btc. |
| `currency` | query | `string` | yes | The fiat or quote currency code for the requested rate. |
