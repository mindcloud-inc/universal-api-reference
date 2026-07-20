# Get CNB Daily Exchange Rates with Směnné kurzy ČNB

Retrieves the last valid daily exchange rates from Směnné kurzy ČNB.

## Endpoint

- **Method:** `GET`
- **Path:** `/exrates/daily`
- **Base URL:** `https://api.cnb.cz/cnbapi`
- **Official documentation:** [Get CNB Daily Exchange Rates](https://api.cnb.cz/cnbapi/swagger-ui.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `date` | no | — |
| `lang` | query | `string` | no | Accepted values: `CZ`, `EN`. |
