# Get SPL XML Document with DailyMed

Retrieves an SPL XML document from DailyMed.

## Endpoint

- **Method:** `GET`
- **Path:** `/spls/{setid}.xml`
- **Base URL:** `https://dailymed.nlm.nih.gov/dailymed/services/v2`
- **Official documentation:** [Get SPL XML Document](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/spls_setid_api.cfm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `setid` | path | `string` | yes | The DailyMed SET ID of the SPL XML document to fetch. |
