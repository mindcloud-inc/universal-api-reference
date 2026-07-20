# Get CNB PRIBOR Daily by Year and Term with Směnné kurzy ČNB

Retrieves PRIBOR data for a year and term from Směnné kurzy ČNB.

## Endpoint

- **Method:** `GET`
- **Path:** `/pribor/daily-year-term`
- **Base URL:** `https://api.cnb.cz/cnbapi`
- **Official documentation:** [Get CNB PRIBOR Daily by Year and Term](https://api.cnb.cz/cnbapi/swagger-ui.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `period` | body | `string` | yes | Accepted values: `NINE_MONTH`, `ONE_DAY`, `ONE_MONTH`, `ONE_WEEK`, `ONE_YEAR`, `SIX_MONTH`, `THREE_MONTH`, `TWO_MONTH`, `TWO_WEEKS`. |
| `year` | body | `number` | no | — |
