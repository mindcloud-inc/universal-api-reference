# List Project Groups with Runrun.it

Retrieves project groups from Runrun.it.

## Endpoint

- **Method:** `GET`
- **Path:** `/clients/:client_id/project_groups`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [List Project Groups](https://runrun.it/api/documentation#project-groups-list-all-project-groups)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | path | `string` | yes | Client Id path parameter. |
