# Get Process Task with Tallyfy

Retrieves a process task from Tallyfy.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:org/runs/:run_id/tasks/:id`
- **Base URL:** `https://api.tallyfy.com`
- **Official documentation:** [Get Process Task](https://tallyfy.com/products/pro/integrations/open-api/code-samples/processes/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Task ID from the selected process. |
| `run_id` | path | `string` | yes | Process ID from Tallyfy. |
