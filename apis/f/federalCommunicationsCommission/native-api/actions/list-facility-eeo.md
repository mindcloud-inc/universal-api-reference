# List Facility EEO with Federal Communications Commission

Retrieves FCC facility EEO records by entity ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/service/{serviceType}/eeo/facilityid/{entityID}`
- **Base URL:** `https://publicfiles.fcc.gov`
- **Official documentation:** [List Facility EEO](https://publicfiles.fcc.gov/json/opif-cdbs.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityID` | path | `string` | no | FCC entity or facility ID. |
| `serviceType` | path | `string` | no | Service type. FCC documents tv, fm, am, cable, sdars, dbs. |
