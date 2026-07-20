# Create Task with Insightful

Creates a new task in your Insightful account.

## Endpoint

- **Method:** `POST`
- **Path:** `/task`
- **Base URL:** `https://app.insightful.io/api/v1`
- **Official documentation:** [Create Task](https://developers.insightful.io/#dd6b68d5-5e70-4404-91bc-ea9898aefb90)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billable` | body | `boolean` | no | Whether the task is billable. |
| `deadline` | body | `number` | no | Task deadline in milliseconds. |
| `description` | body | `string` | no | A description for the task. |
| `employees[]` | body | `array<string>` | yes | Employee IDs to assign to the task. |
| `name` | body | `string` | yes | The task name. |
| `projectId` | body | `string` | yes | The project ID the task belongs to. |
| `status` | body | `string` | no | The task status. |
