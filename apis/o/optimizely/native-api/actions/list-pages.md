# List Pages with Optimizely

Retrieves a list of pages from Optimizely.

## Endpoint

- **Method:** `GET`
- **Path:** `/pages`
- **Base URL:** `https://api.optimizely.com/v2`
- **Official documentation:** [List Pages](https://docs.developers.optimizely.com/web-experimentation/reference/list_pages)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `string` | yes | Filter pages to one project. |
