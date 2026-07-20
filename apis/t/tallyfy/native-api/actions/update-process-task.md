# Update Process Task with Tallyfy

Updates an existing process task in Tallyfy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/organizations/:org/runs/:run_id/tasks/:id`
- **Base URL:** `https://api.tallyfy.com`
- **Official documentation:** [Update Process Task](https://tallyfy.com/products/pro/integrations/open-api/code-samples/processes/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Task ID from the selected process. |
| `run_id` | path | `string` | yes | Process ID from Tallyfy. |
