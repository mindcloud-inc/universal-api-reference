# List Sites By County with Environmental Protection Agency

Retrieves monitoring sites for a county from EPA AQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/list/sitesByCounty`
- **Base URL:** `https://aqs.epa.gov/data/api`
- **Official documentation:** [List Sites By County](https://aqs.epa.gov/aqsweb/documents/data_api.html#lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `state` | query | `string` | yes | Two-digit state FIPS code, including a leading zero when applicable. |
| `county` | query | `string` | yes | Three-digit county FIPS code within the selected state, including leading zeroes when applicable. |
