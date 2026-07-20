# Get Daily Data By State with Environmental Protection Agency

Retrieves daily summary data for a state from EPA AQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/dailyData/byState`
- **Base URL:** `https://aqs.epa.gov/data/api`
- **Official documentation:** [Get Daily Data By State](https://aqs.epa.gov/aqsweb/documents/data_api.html#daily-summary-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `param` | query | `string` | yes | AQS parameter code. EPA allows up to five comma-separated 5-digit parameter codes for most data services. Send multiple values as a string separated by `,`. |
| `bdate` | query | `string` | yes | Begin date in YYYYMMDD format. |
| `edate` | query | `string` | yes | End date in YYYYMMDD format. EPA requires this to be in the same year as the begin date except for monitors. |
| `state` | query | `string` | yes | Two-digit state FIPS code, including a leading zero when applicable. |
| `cbdate` | query | `string` | no | Optional begin date in YYYYMMDD format for filtering by date of last change. |
| `cedate` | query | `string` | no | Optional end date in YYYYMMDD format for filtering by date of last change. |
