# Get QA Annual Performance Evaluations By Site with Environmental Protection Agency

Retrieves QA annual performance evaluations for a site from EPA AQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/qaAnnualPerformanceEvaluations/bySite`
- **Base URL:** `https://aqs.epa.gov/data/api`
- **Official documentation:** [Get QA Annual Performance Evaluations By Site](https://aqs.epa.gov/aqsweb/documents/data_api.html#qa-annual-performance-evaluations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `param` | query | `string` | yes | AQS parameter code. EPA allows up to five comma-separated 5-digit parameter codes for most data services. Send multiple values as a string separated by `,`. |
| `bdate` | query | `string` | yes | Begin date in YYYYMMDD format. |
| `edate` | query | `string` | yes | End date in YYYYMMDD format. EPA requires this to be in the same year as the begin date except for monitors. |
| `state` | query | `string` | yes | Two-digit state FIPS code, including a leading zero when applicable. |
| `county` | query | `string` | yes | Three-digit county FIPS code within the selected state, including leading zeroes when applicable. |
| `site` | query | `string` | yes | Four-digit AQS site number within the selected county, including leading zeroes when applicable. |
