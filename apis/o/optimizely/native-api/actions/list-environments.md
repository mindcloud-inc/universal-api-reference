# List Environments with Optimizely

Retrieves a list of environments from Optimizely.

## Endpoint

- **Method:** `GET`
- **Path:** `/environments`
- **Base URL:** `https://api.optimizely.com/v2`
- **Official documentation:** [List Environments](https://docs.developers.optimizely.com/web-experimentation/reference/list_environments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `string` | yes | Filter environments to one project. |
