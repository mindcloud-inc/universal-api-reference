# Get Stock Peers with Financial Modeling Prep

Retrieves stock peer companies from Financial Modeling Prep.

## Endpoint

- **Method:** `GET`
- **Path:** `/stock-peers`
- **Base URL:** `https://financialmodelingprep.com/stable`
- **Official documentation:** [Get Stock Peers](https://site.financialmodelingprep.com/developer/docs/stable/stock-peers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | query | `string` | yes | Stock ticker symbol, such as AAPL. |
