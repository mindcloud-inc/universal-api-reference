# List Groups with Optimizely

Retrieves exclusion groups from the Optimizely API.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups`
- **Base URL:** `https://api.optimizely.com/v2`
- **Official documentation:** [List Groups](https://docs.developers.optimizely.com/web-experimentation/reference/list_groups)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `string` | yes | Filter groups to one project. |
