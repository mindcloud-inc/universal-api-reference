# Create Run with Roborabbit

Creates a new run for a Roborabbit task.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tasks/:task_uid/runs`
- **Base URL:** `https://api.roborabbit.com`
- **Official documentation:** [Create Run](https://developers.roborabbit.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metadata` | body | `string` | no | Optional metadata to store with the run. |
| `steps[]` | body | `array<object>` | no | Optional array of step override objects for this run. |
| `steps[].action` | body | `string` | no | The action name for the step override. |
| `steps[].config` | body | `object` | no | The config object for the step override. |
| `steps[].skip` | body | `boolean` | no | Set true to skip this step for the run. |
| `steps[].uid` | body | `string` | no | The UID of the task step to override. |
| `task_uid` | path | `string` | yes | The task UID to execute. |
| `webhook_url` | body | `string` | no | Optional URL to receive the completed run object. |
