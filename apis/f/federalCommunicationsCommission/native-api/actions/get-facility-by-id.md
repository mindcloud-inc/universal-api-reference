# Get Facility by ID with Federal Communications Commission

Retrieves an FCC facility by entity ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/service/{serviceType}/facility/id/{entityID}`
- **Base URL:** `https://publicfiles.fcc.gov`
- **Official documentation:** [Get Facility by ID](https://publicfiles.fcc.gov/json/opif-cdbs.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityID` | path | `string` | no | FCC entity or facility ID. |
| `serviceType` | path | `string` | no | Service type. FCC documents tv, fm, am, cable, sdars, dbs. |
