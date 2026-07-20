# Get Macro Indicator with EODHD

Retrieves a macroeconomic indicator by country from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/macro-indicator/{country}`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [Get Macro Indicator](https://eodhd.com/financial-apis/macroeconomics-data-and-macro-indicators-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | path | `string` | yes | Country code accepted by EODHD macro indicators, such as `USA`. |
| `indicator` | query | `string` | yes | Macro indicator code, for example gdp_current_usd. |
