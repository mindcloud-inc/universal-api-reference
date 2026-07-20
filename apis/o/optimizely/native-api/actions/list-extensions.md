# List Extensions with Optimizely

Retrieves a list of extensions from Optimizely.

## Endpoint

- **Method:** `GET`
- **Path:** `/extensions`
- **Base URL:** `https://api.optimizely.com/v2`
- **Official documentation:** [List Extensions](https://docs.developers.optimizely.com/web-experimentation/reference/list_extensions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `string` | yes | Filter extensions to one project. |
