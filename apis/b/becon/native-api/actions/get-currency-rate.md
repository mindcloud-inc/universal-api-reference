# Get Currency Rate with Becon

Retrieves a cryptocurrency-to-fiat exchange rate from Becon.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/currencies/:cryptoCurrencyName`
- **Base URL:** `https://external-api.bcon.global/api`
- **Official documentation:** [Get Currency Rate](https://bcon.global/integrations/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cryptoCurrencyName` | path | `string` | yes | Crypto currency ISO name, for example btc or bnb. |
| `currency` | query | `string` | yes | Target fiat currency ISO name, for example eur or usd. |
