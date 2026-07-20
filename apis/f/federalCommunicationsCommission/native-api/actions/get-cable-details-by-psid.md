# Get Cable Details by PSID with Federal Communications Commission

Retrieves FCC cable details by PSID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/service/cable/psid/{psid}`
- **Base URL:** `https://publicfiles.fcc.gov`
- **Official documentation:** [Get Cable Details by PSID](https://publicfiles.fcc.gov/json/opif-cdbs.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `psid` | path | `string` | no | Cable PSID. |
