# List Facilities by Service Type with Federal Communications Commission

Retrieves FCC facilities by service type.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/service/{serviceType}/facility/getall`
- **Base URL:** `https://publicfiles.fcc.gov`
- **Official documentation:** [List Facilities by Service Type](https://publicfiles.fcc.gov/json/opif-cdbs.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `serviceType` | path | `string` | no | Service type. FCC documents tv, fm, am, cable, sdars, dbs. |
