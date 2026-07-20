# List Task Progress Reports with ITM Platform

## Endpoint

- **Method:** `GET`
- **Path:** `/project/{ProjectId}/task/{TaskId}/progress/`
- **Base URL:** `https://api.itmplatform.com/{company}`
- **Official documentation:** [List Task Progress Reports](https://developers.itmplatform.com/documentation/#/operations/getTaskProgressReports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProjectId` | path | `string` | yes | The ITM Platform project ID. |
| `TaskId` | path | `string` | yes | The ITM Platform task ID. |
