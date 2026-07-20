# List Features with Optimizely

Retrieves a list of features from Optimizely.

## Endpoint

- **Method:** `GET`
- **Path:** `/features`
- **Base URL:** `https://api.optimizely.com/v2`
- **Official documentation:** [List Features](https://docs.developers.optimizely.com/web-experimentation/reference/list_features)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `string` | yes | Filter features to one project. |
