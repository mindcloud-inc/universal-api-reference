# Get Analytics with CheckFlow

## Endpoint

- **Method:** `GET`
- **Path:** `/api/analytics/all`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [Get Analytics](https://docs.checkflow.io/docs/api/analytics#get-analytics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `periodStartDate` | query | `string` | yes | The start of the reporting period in YYYY-MM-DD format. |
| `periodEndDate` | query | `string` | no | The end of the reporting period in YYYY-MM-DD format. If omitted, today is used. |
