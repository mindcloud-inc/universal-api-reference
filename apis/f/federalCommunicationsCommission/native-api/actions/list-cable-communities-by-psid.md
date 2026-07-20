# List Cable Communities by PSID with Federal Communications Commission

Retrieves FCC cable communities by PSID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/service/cable/communities/psid/{psid}`
- **Base URL:** `https://publicfiles.fcc.gov`
- **Official documentation:** [List Cable Communities by PSID](https://publicfiles.fcc.gov/json/opif-cdbs.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `psid` | path | `string` | no | Cable PSID. |
