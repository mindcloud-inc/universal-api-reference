# List Cable EEO with Federal Communications Commission

Retrieves FCC cable EEO records by grouping.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/service/cable/eeo/{groupBy}`
- **Base URL:** `https://publicfiles.fcc.gov`
- **Official documentation:** [List Cable EEO](https://publicfiles.fcc.gov/json/opif-cdbs.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `empUnitId` | query | `string` | no | Array of employee unit IDs for cable EEO lookup. |
| `groupBy` | path | `string` | no | EEO grouping key, such as employee unit ID or form number. |
