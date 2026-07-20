# List Audiences with Optimizely

Retrieves a list of audiences from Optimizely.

## Endpoint

- **Method:** `GET`
- **Path:** `/audiences`
- **Base URL:** `https://api.optimizely.com/v2`
- **Official documentation:** [List Audiences](https://docs.developers.optimizely.com/web-experimentation/reference/list_audiences)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `string` | yes | Filter audiences to one project. |
