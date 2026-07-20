# Get Market Statistics with RentCast

Retrieves market statistics from RentCast for a ZIP code.

## Endpoint

- **Method:** `GET`
- **Path:** `/markets`
- **Base URL:** `https://api.rentcast.io/v1`
- **Official documentation:** [Get Market Statistics](https://developers.rentcast.io/reference/market-statistics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zipCode` | query | `string` | yes | A valid 5-digit US zip code. |
| `dataType` | query | `list<string>` | no | The type of aggregate market data to retrieve. Accepted values: `All`, `Rental`, `Sale`. |
| `historyRange` | query | `number` | no | The number of months of historical market data to include. |
