# List Time Series Rates with Exchange Rates API

Retrieves time-series exchange rates from Exchange Rates API.

## Endpoint

- **Method:** `GET`
- **Path:** `timeseries`
- **Base URL:** `https://api.exchangeratesapi.io/v1`
- **Official documentation:** [List Time Series Rates](https://exchangeratesapi.io/documentation/#time-series-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `date` | yes | Start date of the time frame in YYYY-MM-DD format. |
| `end_date` | query | `date` | yes | End date of the time frame in YYYY-MM-DD format. |
| `base` | query | `string` | no | Optional three-letter currency code for the base currency. Defaults to EUR when omitted. |
| `symbols` | query | `string` | no | Optional comma-separated currency codes to limit the returned rates, such as USD,CAD,JPY. Send multiple values as a string separated by `,`. |
