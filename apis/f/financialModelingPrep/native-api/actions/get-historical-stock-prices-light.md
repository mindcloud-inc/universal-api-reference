# Get Historical Stock Prices Light with Financial Modeling Prep

Retrieves light historical stock prices from Financial Modeling Prep.

## Endpoint

- **Method:** `GET`
- **Path:** `/historical-price-eod/light`
- **Base URL:** `https://financialmodelingprep.com/stable`
- **Official documentation:** [Get Historical Stock Prices Light](https://site.financialmodelingprep.com/developer/docs/stable/historical-price-eod-light)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | query | `string` | yes | Stock ticker symbol, such as AAPL. |
