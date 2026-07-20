# Set Task Metadata with Scale

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/task/metadata`
- **Base URL:** `https://api.scale.com`
- **Official documentation:** [Set Task Metadata](https://docs.genai.scale.com/v2/task-set-metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metadata` | body | `string` | yes | Metadata object to store on the task. |
| `task_id` | body | `string` | yes | The task identifier. |
