# Reopen Process Task with Tallyfy

Reopens a completed process task in Tallyfy.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/organizations/:org/runs/:run_id/completed-tasks/:task_id`
- **Base URL:** `https://api.tallyfy.com`
- **Official documentation:** [Reopen Process Task](https://tallyfy.com/products/pro/integrations/open-api/code-samples/processes/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | path | `string` | yes | Process ID from Tallyfy. |
| `task_id` | path | `string` | yes | Completed task ID from the selected process. |
