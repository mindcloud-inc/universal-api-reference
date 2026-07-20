# Get USDT to USD Rate with Becon

Retrieves the USDT-to-USD rate from Becon.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/currencies/:cryptoCurrencyName`
- **Base URL:** `https://external-api.bcon.global/api`
- **Official documentation:** [Get USDT to USD Rate](https://bcon.global/integrations/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cryptoCurrencyName` | path | `string` | yes | The cryptocurrency code in the path, such as usdt. |
| `currency` | query | `string` | yes | The fiat or quote currency code for the requested rate. |
