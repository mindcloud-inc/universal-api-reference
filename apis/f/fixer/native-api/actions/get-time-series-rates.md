# Get Time Series Rates with Fixer

Retrieves time-series exchange rates from Fixer.

## Endpoint

- **Method:** `GET`
- **Path:** `/timeseries`
- **Base URL:** `https://data.fixer.io/api`
- **Official documentation:** [Get Time Series Rates](https://fixer.io/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | yes | Start date in YYYY-MM-DD format. |
| `end_date` | query | `string` | yes | End date in YYYY-MM-DD format. |
| `symbols` | query | `string` | no | Optional comma-separated list of currency codes to limit the returned rates. |
| `base` | query | `string` | no | Optional three-letter base currency code. Fixer defaults to EUR and some plans restrict custom base currencies. |
