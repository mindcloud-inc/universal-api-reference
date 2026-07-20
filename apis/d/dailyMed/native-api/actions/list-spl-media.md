# List SPL Media with DailyMed

Retrieves SPL media from DailyMed.

## Endpoint

- **Method:** `GET`
- **Path:** `/spls/{setid}/media.json`
- **Base URL:** `https://dailymed.nlm.nih.gov/dailymed/services/v2`
- **Official documentation:** [List SPL Media](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/spls_setid_media_api.cfm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `setid` | path | `string` | yes | The DailyMed SET ID of the SPL whose media links should be returned. |
