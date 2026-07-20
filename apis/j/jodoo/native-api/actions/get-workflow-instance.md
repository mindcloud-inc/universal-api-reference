# Get Workflow Instance with Jodoo

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.jodoo.com/api/v6/workflow/instance/get`
- **Base URL:** `https://api.jodoo.com/api/v5`
- **Official documentation:** [Get Workflow Instance](https://help.jodoo.com/en/articles/9992396-workflow-instances-query-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `instance_id` | body | `string` | yes | Workflow instance ID, which is the same value as the workflow record data ID. |
| `tasks_type` | body | `number` | yes | Type of embedded task data to return. Use `0` to omit tasks or `1` to return all workflow tasks. |
