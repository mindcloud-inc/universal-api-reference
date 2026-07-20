# Check File Task with Feishu Drive

Retrieves a file task status from Feishu Drive.

## Endpoint

- **Method:** `GET`
- **Path:** `/drive/v1/files/task_check`
- **Base URL:** `https://open.feishu.cn/open-apis`
- **Official documentation:** [Check File Task](https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/task_check)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | query | `string` | yes | Async task identifier returned by delete or move folder operations. |
