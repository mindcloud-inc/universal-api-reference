# Get Historical Exchange Rates with Fixer

Retrieves historical exchange rates from Fixer by date.

## Endpoint

- **Method:** `GET`
- **Path:** `/:date`
- **Base URL:** `https://data.fixer.io/api`
- **Official documentation:** [Get Historical Exchange Rates](https://fixer.io/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | path | `string` | yes | Historical date in YYYY-MM-DD format. |
| `symbols` | query | `string` | no | Optional comma-separated list of currency codes to limit the returned rates. |
| `base` | query | `string` | no | Optional three-letter base currency code. Fixer defaults to EUR and some plans restrict custom base currencies. |
