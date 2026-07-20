# Get Task Details with CheckFlow

## Endpoint

- **Method:** `GET`
- **Path:** `/api/task/details`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [Get Task Details](https://docs.checkflow.io/docs/api/tasks#get-task-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checklistId` | query | `number` | yes | The ID of the checklist that contains the task. |
| `taskKey` | query | `string` | yes | The key of the task. |
