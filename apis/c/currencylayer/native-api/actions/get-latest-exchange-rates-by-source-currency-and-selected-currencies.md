# Get Latest Exchange Rates By Source Currency And Selected Currencies with Currencylayer

Retrieves latest exchange rates by source and selected currencies from Currencylayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/live`
- **Base URL:** `https://api.currencylayer.com`
- **Official documentation:** [Get Latest Exchange Rates By Source Currency And Selected Currencies](https://currencylayer.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | query | `string` | yes | 3-letter source currency code. |
| `currencies` | query | `string` | yes | Comma-separated 3-letter currency codes to limit the returned rates. |
