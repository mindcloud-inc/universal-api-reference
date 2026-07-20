# Get Broadcast Contour with Federal Communications Commission

Retrieves FCC broadcast contour data by service and identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/contour/{serviceType}/{idType}/{idValue}.{format}`
- **Base URL:** `https://publicfiles.fcc.gov`
- **Official documentation:** [Get Broadcast Contour](https://publicfiles.fcc.gov/json/opif-contour-apis.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | path | `string` | no | Response format. FCC documents json, jsonp, shp, kml, gml, csv. Use json for normal API runs. |
| `idType` | path | `string` | no | Identifier type. Valid values include facilityid, callsign, filenumber, applicationid, antennaid. |
| `idValue` | path | `string` | no | Identifier value for the selected ID type. |
| `serviceType` | path | `string` | no | Contour service type. Valid values documented by FCC: tv, fm, am. |
| `stationClass` | query | `string` | no | AM-only station class; ignored for TV and FM. |
| `timePeriod` | query | `string` | no | AM-only time period; FCC currently documents day. |
