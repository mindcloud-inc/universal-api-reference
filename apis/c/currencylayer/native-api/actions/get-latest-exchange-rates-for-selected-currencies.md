# Get Latest Exchange Rates For Selected Currencies with Currencylayer

Retrieves latest exchange rates for selected currencies from Currencylayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/live`
- **Base URL:** `https://api.currencylayer.com`
- **Official documentation:** [Get Latest Exchange Rates For Selected Currencies](https://currencylayer.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currencies` | query | `string` | yes | Comma-separated 3-letter currency codes to limit the returned rates. |
