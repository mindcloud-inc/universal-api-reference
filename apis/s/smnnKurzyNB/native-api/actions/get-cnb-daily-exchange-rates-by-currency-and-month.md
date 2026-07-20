# Get CNB Daily Exchange Rates by Currency and Month with Směnné kurzy ČNB

Retrieves daily exchange rates for a currency and month from Směnné kurzy ČNB.

## Endpoint

- **Method:** `GET`
- **Path:** `/exrates/daily-currency-month`
- **Base URL:** `https://api.cnb.cz/cnbapi`
- **Official documentation:** [Get CNB Daily Exchange Rates by Currency and Month](https://api.cnb.cz/cnbapi/swagger-ui.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `currency` | query | `string` | yes |
| `yearMonth` | query | `string` | no |
