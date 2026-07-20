# Create Action Plan with Procore

Creates a new action plan in Procore.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v1.0/projects/:project_id/action_plans/plans`
- **Base URL:** `https://api.procore.com`
- **Official documentation:** [Create Action Plan](https://developers.procore.com/reference/rest/action-plans#create-action-plan)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `plan` | body | `object` | yes | Action plan payload object. |
| `project_id` | path | `string` | yes | Unique identifier for the project. |
