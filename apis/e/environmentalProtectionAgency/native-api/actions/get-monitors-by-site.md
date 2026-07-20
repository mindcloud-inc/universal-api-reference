# Get Monitors By Site with Environmental Protection Agency

Retrieves monitors for a site from EPA AQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/monitors/bySite`
- **Base URL:** `https://aqs.epa.gov/data/api`
- **Official documentation:** [Get Monitors By Site](https://aqs.epa.gov/aqsweb/documents/data_api.html#monitors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `param` | query | `string` | no | Optional AQS parameter code filter. Use up to five comma-separated 5-digit parameter codes. Send multiple values as a string separated by `,`. |
| `bdate` | query | `string` | yes | Begin date in YYYYMMDD format. |
| `edate` | query | `string` | yes | End date in YYYYMMDD format. EPA requires this to be in the same year as the begin date except for monitors. |
| `state` | query | `string` | yes | Two-digit state FIPS code, including a leading zero when applicable. |
| `county` | query | `string` | yes | Three-digit county FIPS code within the selected state, including leading zeroes when applicable. |
| `site` | query | `string` | yes | Four-digit AQS site number within the selected county, including leading zeroes when applicable. |
| `cbdate` | query | `string` | no | Optional begin date in YYYYMMDD format for filtering by date of last change. |
| `cedate` | query | `string` | no | Optional end date in YYYYMMDD format for filtering by date of last change. |
