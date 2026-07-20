# Get Service Relationship by FRN with Federal Communications Commission

Retrieves FCC service relationships by FRN.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/service/{serviceType}/relationship/frn/{frn}`
- **Base URL:** `https://publicfiles.fcc.gov`
- **Official documentation:** [Get Service Relationship by FRN](https://publicfiles.fcc.gov/json/opif-cdbs.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `frn` | path | `string` | no | FCC Registration Number; documented as 10 digits. |
| `serviceType` | path | `string` | no | Broadcast service type. Valid values documented by FCC: tv, fm, am. |
