# Get Location Status with WeBeHome

## Endpoint

- **Method:** `POST`
- **Path:** `OpenAPIservice.svc/Location/GetStatus3`
- **Base URL:** `https://webehome.com/API`
- **Official documentation:** [Get Location Status](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `BaseUnitID` | body | `string` | yes | Location ID. If 0 or omitted, the first location the user can access is used. |
| `ClusterID` | body | `string` | yes | Cluster ID for the location when BaseUnitID is supplied. |
| `SubUnitID` | body | `string` | no | Optional device ID to limit the response to one accessory. |
| `Hash` | body | `string` | no | Last hash from previous return value, empty when none was received. |
