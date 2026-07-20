# Check Upload Status with LOBSTR.IO

Retrieves upload task status from LOBSTR.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/tasks/upload/:upload_task_id`
- **Base URL:** `https://api.lobstr.io`
- **Official documentation:** [Check Upload Status](https://docs.lobstr.io/docs/check-upload-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `upload_task_id` | path | `string` | yes | The upload task ID returned by Upload Tasks. |
