# List Sessions with LambdaTest

Retrieves sessions from LambdaTest.

## Endpoint

- **Method:** `GET`
- **Path:** `/sessions`
- **Base URL:** `https://api.lambdatest.com/automation/api/v1`
- **Official documentation:** [List Sessions](https://swagger-api-support.lambdatest.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of sessions to return. |
| `status` | query | `string` | no | Comma-separated LambdaTest session statuses to filter by. |
| `test_name` | query | `string` | no | Filter sessions by test name. |
| `username` | query | `string` | no | Filter sessions by LambdaTest username. |
| `offset` | query | `number` | no | Number of sessions to skip before returning results. |
| `build_id` | query | `string` | no | Filter sessions by build ID. |
