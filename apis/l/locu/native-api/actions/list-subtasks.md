# List Subtasks with Locu

Retrieves subtasks for a task from Locu.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/:id/subtasks`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [List Subtasks](https://locu.app/api/docs#tag/tasks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Parent task ID |
| `done` | query | `string` | no | Filter subtasks by completion flag Accepted values: `0`, `1`. |
| `includeHtml` | query | `boolean` | no | Include description content as HTML |
| `includeMarkdown` | query | `boolean` | no | Include description content as Markdown |
| `includePlainText` | query | `boolean` | no | Include description content as plain text |
| `includeJson` | query | `boolean` | no | Include description content as structured JSON |
