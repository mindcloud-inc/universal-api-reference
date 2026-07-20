# List Process Tasks with Tallyfy

Retrieves tasks for a process in Tallyfy.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:org/runs/:run_id/tasks`
- **Base URL:** `https://api.tallyfy.com`
- **Official documentation:** [List Process Tasks](https://tallyfy.com/products/pro/integrations/open-api/code-samples/processes/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | path | `string` | yes | Process ID from Tallyfy. |
