# Get DBS Entity by FRN with Federal Communications Commission

Retrieves FCC DBS entity details by FRN.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/service/dbs/frn/{frn}`
- **Base URL:** `https://publicfiles.fcc.gov`
- **Official documentation:** [Get DBS Entity by FRN](https://publicfiles.fcc.gov/json/opif-cdbs.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `frn` | path | `string` | no | FCC Registration Number; documented as 10 digits. |
