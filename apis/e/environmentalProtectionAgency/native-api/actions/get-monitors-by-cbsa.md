# Get Monitors By CBSA with Environmental Protection Agency

Retrieves monitors for a CBSA from EPA AQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/monitors/byCBSA`
- **Base URL:** `https://aqs.epa.gov/data/api`
- **Official documentation:** [Get Monitors By CBSA](https://aqs.epa.gov/aqsweb/documents/data_api.html#monitors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `param` | query | `string` | no | Optional AQS parameter code filter. Use up to five comma-separated 5-digit parameter codes. Send multiple values as a string separated by `,`. |
| `bdate` | query | `string` | yes | Begin date in YYYYMMDD format. |
| `edate` | query | `string` | yes | End date in YYYYMMDD format. EPA requires this to be in the same year as the begin date except for monitors. |
| `cbsa` | query | `string` | yes | Five-digit Core Based Statistical Area code. |
| `cbdate` | query | `string` | no | Optional begin date in YYYYMMDD format for filtering by date of last change. |
| `cedate` | query | `string` | no | Optional end date in YYYYMMDD format for filtering by date of last change. |
