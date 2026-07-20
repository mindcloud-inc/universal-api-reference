# List Links with ShortPen

Retrieves links from ShortPen for a specific workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/links`
- **Base URL:** `https://api.shortpen.com`
- **Official documentation:** [List Links](https://shortpen.com/docs/api-reference/endpoint/list-links)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | query | `number` | no | Workspace ID to scope the returned links to. |
