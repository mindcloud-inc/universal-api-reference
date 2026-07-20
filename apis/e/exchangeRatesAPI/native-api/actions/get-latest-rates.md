# Get Latest Rates with Exchange Rates API

Retrieves latest exchange rates from Exchange Rates API.

## Endpoint

- **Method:** `GET`
- **Path:** `latest`
- **Base URL:** `https://api.exchangeratesapi.io/v1`
- **Official documentation:** [Get Latest Rates](https://exchangeratesapi.io/documentation/#latest-rates-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `base` | query | `string` | no | Optional three-letter currency code for the base currency. Defaults to EUR when omitted. |
| `symbols` | query | `string` | no | Optional comma-separated currency codes to limit the returned rates, such as USD,CAD,JPY. Send multiple values as a string separated by `,`. |
