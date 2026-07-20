# Get CNB FX Rates by Month with Směnné kurzy ČNB

Retrieves daily FX rates for a month from Směnné kurzy ČNB.

## Endpoint

- **Method:** `GET`
- **Path:** `/fxrates/daily-month`
- **Base URL:** `https://api.cnb.cz/cnbapi`
- **Official documentation:** [Get CNB FX Rates by Month](https://api.cnb.cz/cnbapi/swagger-ui.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lang` | query | `string` | no | Accepted values: `CZ`, `EN`. |
| `yearMonth` | query | `string` | no | — |
