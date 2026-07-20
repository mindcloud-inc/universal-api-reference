# Get CNB FX Rates by Year with Směnné kurzy ČNB

Retrieves daily FX rates for a year from Směnné kurzy ČNB.

## Endpoint

- **Method:** `GET`
- **Path:** `/fxrates/daily-year`
- **Base URL:** `https://api.cnb.cz/cnbapi`
- **Official documentation:** [Get CNB FX Rates by Year](https://api.cnb.cz/cnbapi/swagger-ui.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lang` | query | `string` | no | Accepted values: `CZ`, `EN`. |
| `year` | query | `number` | no | — |
