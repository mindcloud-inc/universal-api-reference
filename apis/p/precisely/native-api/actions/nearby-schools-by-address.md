# Nearby Schools By Address with Precisely

Retrieves nearby schools from Precisely by address.

## Endpoint

- **Method:** `GET`
- **Path:** `/schools/v1/school/byaddress`
- **Base URL:** `https://api.precisely.com`
- **Official documentation:** [Nearby Schools By Address](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/Schools/School_ByAddress/school_byaddress.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | query | `string` | yes | Single-line street address to search near. |
| `schoolType` | query | `string` | no | Provider school type code filter. |
| `edLevel` | query | `string` | no | Provider education level code filter. |
| `schoolSubType` | query | `string` | no | Provider school subtype code filter. |
| `gender` | query | `string` | no | Provider gender code filter. |
| `assignedSchoolsOnly` | query | `boolean` | no | Return only schools assigned to the address. |
| `districtSchoolsOnly` | query | `boolean` | no | Return only schools in the serving district. |
| `searchRadius` | query | `number` | no | Radius around the address to search. |
| `searchRadiusUnit` | query | `string` | no | Unit for the search radius. |
| `travelTime` | query | `number` | no | Travel time threshold around the address. |
| `travelTimeUnit` | query | `string` | no | Unit for the travel time. |
| `travelMode` | query | `string` | no | Travel mode used for school proximity calculations. |
| `travelDistance` | query | `number` | no | Travel distance threshold around the address. |
| `travelDistanceUnit` | query | `string` | no | Unit for the travel distance. |
| `maxCandidates` | query | `number` | no | Maximum number of schools to return. |
