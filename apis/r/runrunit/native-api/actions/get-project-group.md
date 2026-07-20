# Get Project Group with Runrun.it

Retrieves a project group from Runrun.it.

## Endpoint

- **Method:** `GET`
- **Path:** `/clients/:client_id/project_groups/:id`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [Get Project Group](https://runrun.it/api/documentation#project-groups-show-a-project-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | path | `string` | yes | Client Id path parameter. |
| `id` | path | `string` | yes | Id path parameter. |
