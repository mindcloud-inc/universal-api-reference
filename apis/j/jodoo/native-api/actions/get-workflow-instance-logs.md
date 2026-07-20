# Get Workflow Instance Logs with Jodoo

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.jodoo.com/api/v1/workflow/instance/logs`
- **Base URL:** `https://api.jodoo.com/api/v5`
- **Official documentation:** [Get Workflow Instance Logs](https://help.jodoo.com/en/articles/9992397-workflow-instance-logs-query-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `instance_id` | body | `string` | yes | Workflow instance ID, which is the same value as the workflow record data ID. |
| `types[]` | body | `array<string>` | yes | Array of workflow log types to return, such as `comment` or `operate`. |
| `skip` | body | `number` | no | Number of logs to skip before returning results. |
| `limit` | body | `number` | no | Maximum number of logs to return. |
