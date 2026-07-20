# List Folders with ShortPen

Retrieves folders from ShortPen for a specific workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/get`
- **Base URL:** `https://api.shortpen.com`
- **Official documentation:** [List Folders](https://shortpen.com/docs/api-reference/endpoint/get-resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | body | `number` | no | Workspace scope used for folder lookups. |
