# Get CNB FX Rates by Currency and Month Range with Směnné kurzy ČNB

Retrieves daily FX rates for a currency and month range from Směnné kurzy ČNB.

## Endpoint

- **Method:** `GET`
- **Path:** `/fxrates/daily-range-currency`
- **Base URL:** `https://api.cnb.cz/cnbapi`
- **Official documentation:** [Get CNB FX Rates by Currency and Month Range](https://api.cnb.cz/cnbapi/swagger-ui.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currency` | query | `string` | yes | — |
| `lang` | query | `string` | no | Accepted values: `CZ`, `EN`. |
| `yearMonthFrom` | query | `string` | no | — |
| `yearMonthTo` | query | `string` | no | — |
