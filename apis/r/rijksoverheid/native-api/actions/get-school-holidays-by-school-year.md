# Get School Holidays By School Year with Rijksoverheid

Retrieves school holidays for a school year from Rijksoverheid.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/infotypes/schoolholidays/schoolyear/{{schoolYear}}`
- **Base URL:** `https://opendata.rijksoverheid.nl`
- **Official documentation:** [Get School Holidays By School Year](https://www.rijksoverheid.nl/opendata/schoolvakanties)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schoolYear` | path | `string` | yes | School year to retrieve in YYYY-YYYY format, for example 2029-2030. |
