# Get BNB to EUR Rate with Becon

Retrieves the BNB-to-EUR rate from Becon.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/currencies/:cryptoCurrencyName`
- **Base URL:** `https://external-api.bcon.global/api`
- **Official documentation:** [Get BNB to EUR Rate](https://bcon.global/integrations/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cryptoCurrencyName` | path | `string` | yes | The cryptocurrency code in the path, such as bnb. |
| `currency` | query | `string` | yes | The fiat or quote currency code for the requested rate. |
