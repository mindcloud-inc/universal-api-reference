# Get Latest Exchange Rates with Fixer

Retrieves latest exchange rates from Fixer.

## Endpoint

- **Method:** `GET`
- **Path:** `/latest`
- **Base URL:** `https://data.fixer.io/api`
- **Official documentation:** [Get Latest Exchange Rates](https://fixer.io/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbols` | query | `string` | no | Optional comma-separated list of currency codes to limit the returned rates. |
| `base` | query | `string` | no | Optional three-letter base currency code. Fixer defaults to EUR and some plans restrict custom base currencies. |
