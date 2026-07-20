# Get CNB Daily Exchange Rates by Year with Směnné kurzy ČNB

Retrieves daily exchange rates for a year from Směnné kurzy ČNB.

## Endpoint

- **Method:** `GET`
- **Path:** `/exrates/daily-year`
- **Base URL:** `https://api.cnb.cz/cnbapi`
- **Official documentation:** [Get CNB Daily Exchange Rates by Year](https://api.cnb.cz/cnbapi/swagger-ui.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | — |
| `lang` | query | `string` | no | Accepted values: `CZ`, `EN`. |
