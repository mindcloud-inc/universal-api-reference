# Get SDARS EEO by Facility with Federal Communications Commission

Retrieves FCC SDARS EEO records by facility ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/service/sdars/eeo/facility/{facilityID}`
- **Base URL:** `https://publicfiles.fcc.gov`
- **Official documentation:** [Get SDARS EEO by Facility](https://publicfiles.fcc.gov/json/opif-cdbs.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `facilityID` | path | `string` | no | SDARS facility ID. |
