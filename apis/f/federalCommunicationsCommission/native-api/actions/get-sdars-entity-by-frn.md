# Get SDARS Entity by FRN with Federal Communications Commission

Retrieves FCC SDARS entity details by FRN.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/service/sdars/frn/{frn}`
- **Base URL:** `https://publicfiles.fcc.gov`
- **Official documentation:** [Get SDARS Entity by FRN](https://publicfiles.fcc.gov/json/opif-cdbs.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `frn` | path | `string` | no | FCC Registration Number; documented as 10 digits. |
