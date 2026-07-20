# Get Country Lookup with Greip - Fraud Prevention

Retrieves country lookup data from Greip.

## Endpoint

- **Method:** `GET`
- **Path:** `/lookup/country`
- **Base URL:** `https://greipapi.com`
- **Official documentation:** [Get Country Lookup](https://docs.greip.io/api-reference/endpoint/data-lookup/country)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CountryCode` | query | `string` | yes | The ISO 3166-1 alpha-2 country code to look up. |
| `params` | query | `string` | no | Comma-separated modules to include, such as language, flag, currency, or timezone. |
