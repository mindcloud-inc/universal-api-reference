# List Action Plans with Procore

Retrieves action plans from Procore.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v1.0/projects/:project_id/action_plans/plans`
- **Base URL:** `https://api.procore.com`
- **Official documentation:** [List Action Plans](https://developers.procore.com/reference/rest/action-plans#list-action-plans)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Unique identifier for the project. |
