# List Task Controls with CheckFlow

## Endpoint

- **Method:** `GET`
- **Path:** `/api/template/task-content`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [List Task Controls](https://docs.checkflow.io/docs/api/templates#list-task-controls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskKey` | query | `string` | yes | The key of the task. Use Get Template Tasks to find the key. |
| `contentType` | query | `string` | no | Filters results by control type. Use ALL to return every control. |
