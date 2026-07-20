# Get Work Item with Kelloo

Retrieves a work item from Kelloo.

## Endpoint

- **Method:** `GET`
- **Path:** `/WorkItem`
- **Base URL:** `https://plan.kelloo.com/api`
- **Official documentation:** [Get Work Item](https://documenter.getpostman.com/view/14463756/UzBgtpF8#d4820d69-cce1-4c02-a5a4-cd70f7dfff81)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenario_id` | query | `string` | yes | The Kelloo scenario ID that owns the work item. |
| `id` | query | `string` | yes | The Kelloo work item ID to retrieve. |
