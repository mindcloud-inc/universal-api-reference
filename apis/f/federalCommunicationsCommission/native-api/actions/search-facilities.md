# Search Facilities with Federal Communications Commission

Retrieves FCC facilities matching a keyword.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/service/facility/search/{keyword}`
- **Base URL:** `https://publicfiles.fcc.gov`
- **Official documentation:** [Search Facilities](https://publicfiles.fcc.gov/json/opif-cdbs.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | path | `string` | no | Facility search keyword. |
