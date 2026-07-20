# List Facility Applications with Federal Communications Commission

Retrieves FCC facility applications by entity ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/service/{serviceType}/applications/facility/{entityID}`
- **Base URL:** `https://publicfiles.fcc.gov`
- **Official documentation:** [List Facility Applications](https://publicfiles.fcc.gov/json/opif-cdbs.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityID` | path | `string` | no | FCC entity or facility ID. |
| `serviceType` | path | `string` | no | Service type. FCC documents tv, fm, am, cable, sdars, dbs. |
