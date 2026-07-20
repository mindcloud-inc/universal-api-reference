# Get Task Response Attachment URL with Scale

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/datasets/task/{task_id}/response_url/{attachment_id}`
- **Base URL:** `https://api.scale.com`
- **Official documentation:** [Get Task Response Attachment URL](https://docs.genai.scale.com/v2/datasets-response_url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachment_id` | path | `string` | yes | The attachment identifier. |
| `task_id` | path | `string` | yes | The task identifier. |
