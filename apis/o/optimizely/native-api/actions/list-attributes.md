# List Attributes with Optimizely

Retrieves a list of attributes from Optimizely.

## Endpoint

- **Method:** `GET`
- **Path:** `/attributes`
- **Base URL:** `https://api.optimizely.com/v2`
- **Official documentation:** [List Attributes](https://docs.developers.optimizely.com/web-experimentation/reference/list_attributes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `string` | yes | Filter attributes to one project. |
