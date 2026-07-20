# List SPL NDCs with DailyMed

Retrieves NDCs for an SPL from DailyMed.

## Endpoint

- **Method:** `GET`
- **Path:** `/spls/{setid}/ndcs.json`
- **Base URL:** `https://dailymed.nlm.nih.gov/dailymed/services/v2`
- **Official documentation:** [List SPL NDCs](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/spls_setid_ndcs_api.cfm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `setid` | path | `string` | yes | The DailyMed SET ID of the SPL whose associated NDCs should be returned. |
