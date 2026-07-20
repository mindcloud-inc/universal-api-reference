# Get Historical Rates with Exchange Rates API

Retrieves historical exchange rates from Exchange Rates API.

## Endpoint

- **Method:** `GET`
- **Path:** `:date`
- **Base URL:** `https://api.exchangeratesapi.io/v1`
- **Official documentation:** [Get Historical Rates](https://exchangeratesapi.io/documentation/#historical-rates-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | path | `date` | yes | Past date for the requested historical rates in YYYY-MM-DD format. |
| `base` | query | `string` | no | Optional three-letter currency code for the base currency. Defaults to EUR when omitted. |
| `symbols` | query | `string` | no | Optional comma-separated currency codes to limit the returned rates, such as USD,CAD,JPY. Send multiple values as a string separated by `,`. |
