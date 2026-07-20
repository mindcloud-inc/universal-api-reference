# Get Bulk Verification Result with EmailVerify.io

Retrieves a bulk verification task result from EmailVerify.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/get-result-bulk-verification-task/`
- **Base URL:** `https://app.emailverify.io/api/v1`
- **Official documentation:** [Get Bulk Verification Result](https://www.emailverify.io/api/docs/#bulk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | query | `string` | yes | Bulk verification task identifier returned when the task was created. |
