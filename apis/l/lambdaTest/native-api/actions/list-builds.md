# List Builds with LambdaTest

Retrieves builds from LambdaTest.

## Endpoint

- **Method:** `GET`
- **Path:** `/builds`
- **Base URL:** `https://api.lambdatest.com/automation/api/v1`
- **Official documentation:** [List Builds](https://swagger-api-support.lambdatest.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of builds to return. |
| `offset` | query | `number` | no | Number of builds to skip before returning results. |
| `status` | query | `string` | no | Comma-separated LambdaTest build statuses to filter by. |
| `fromdate` | query | `string` | no | Start date in YYYY-MM-DD format. |
| `todate` | query | `string` | no | End date in YYYY-MM-DD format. |
| `sort` | query | `string` | no | Sort expression such as asc.user_id or desc.end_time. |
