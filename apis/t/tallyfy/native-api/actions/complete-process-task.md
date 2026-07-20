# Complete Process Task with Tallyfy

Completes a process task in Tallyfy.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:org/runs/:run_id/completed-tasks`
- **Base URL:** `https://api.tallyfy.com`
- **Official documentation:** [Complete Process Task](https://tallyfy.com/products/pro/integrations/open-api/code-samples/processes/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | path | `string` | yes | Process ID from Tallyfy. |
