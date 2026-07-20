# Get Forex Rates with Finnhub

Retrieves forex rates from Finnhub.

## Endpoint

- **Method:** `GET`
- **Path:** `/forex/rates`
- **Base URL:** `https://finnhub.io/api/v1`
- **Official documentation:** [Get Forex Rates](https://finnhub.io/docs/api#forex-rates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `base` | query | `string` | no | Optional base currency, such as USD. |
| `date` | query | `string` | no | Exchange-rate date in YYYY-MM-DD format. |
