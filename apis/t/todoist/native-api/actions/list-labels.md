# List Labels with Todoist

Retrieves labels from Todoist.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/labels`
- **Base URL:** `https://api.todoist.com`
- **Official documentation:** [List Labels](https://developer.todoist.com/api/v1/#tag/Labels/operation/get_labels_api_v1_labels_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Cursor for the next page of results. |
| `limit` | query | `number` | no | Maximum number of results to return. |
