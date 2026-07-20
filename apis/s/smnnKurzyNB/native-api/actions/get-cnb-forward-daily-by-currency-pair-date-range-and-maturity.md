# Get CNB Forward Daily by Currency Pair, Date Range, and Maturity with Směnné kurzy ČNB

Retrieves forward rates by currency pair, date range, and maturity from Směnné kurzy ČNB.

## Endpoint

- **Method:** `GET`
- **Path:** `/forward/daily-range-currency-pair-maturity`
- **Base URL:** `https://api.cnb.cz/cnbapi`
- **Official documentation:** [Get CNB Forward Daily by Currency Pair, Date Range, and Maturity](https://api.cnb.cz/cnbapi/swagger-ui.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currencyPair` | body | `string` | yes | Accepted values: `ALL`, `EUR_TO_CZK`, `USD_TO_CZK`. |
| `dateFrom` | body | `date` | yes | — |
| `dateTo` | body | `date` | no | — |
| `maturity` | body | `string` | yes | Accepted values: `ALL`, `SIX_MONTH`, `THREE_MONTH`. |
