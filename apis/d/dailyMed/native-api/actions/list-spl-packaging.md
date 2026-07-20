# List SPL Packaging with DailyMed

Retrieves SPL packaging details from DailyMed.

## Endpoint

- **Method:** `GET`
- **Path:** `/spls/{setid}/packaging.json`
- **Base URL:** `https://dailymed.nlm.nih.gov/dailymed/services/v2`
- **Official documentation:** [List SPL Packaging](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/spls_setid_packaging_api.cfm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `setid` | path | `string` | yes | The DailyMed SET ID of the SPL whose packaging details should be returned. |
