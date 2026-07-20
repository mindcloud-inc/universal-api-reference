# List SPL History with DailyMed

Retrieves SPL version history from DailyMed.

## Endpoint

- **Method:** `GET`
- **Path:** `/spls/{setid}/history.json`
- **Base URL:** `https://dailymed.nlm.nih.gov/dailymed/services/v2`
- **Official documentation:** [List SPL History](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/spls_setid_history_api.cfm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `setid` | path | `string` | yes | The DailyMed SET ID of the SPL whose version history should be returned. |
