# Create task template from call with Vibrato

Creates a task template from a Vibrato call.

## Endpoint

- **Method:** `POST`
- **Path:** `/task_templates/create_from_call/`
- **Base URL:** `https://api.getvibrato.com/api/v1`
- **Official documentation:** [Create task template from call](https://docs.getvibrato.com/api-reference/tasktemplates/create-a-task-template-from-a-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `call_id` | body | `number` | yes | Source call ID. |
