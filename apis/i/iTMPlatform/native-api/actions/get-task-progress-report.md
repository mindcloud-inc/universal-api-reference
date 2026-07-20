# Get Task Progress Report with ITM Platform

## Endpoint

- **Method:** `GET`
- **Path:** `/project/{ProjectId}/task/{TaskId}/progress/{TaskProgressId}`
- **Base URL:** `https://api.itmplatform.com/{company}`
- **Official documentation:** [Get Task Progress Report](https://developers.itmplatform.com/documentation/#/operations/getATaskProgressReport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProjectId` | path | `string` | yes | The ITM Platform project ID. |
| `TaskId` | path | `string` | yes | The ITM Platform task ID. |
| `TaskProgressId` | path | `string` | yes | The ITM Platform task progress report ID. |
