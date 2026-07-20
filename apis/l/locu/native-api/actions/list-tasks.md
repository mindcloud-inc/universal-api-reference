# List Tasks with Locu

Retrieves a paginated list of tasks from Locu.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [List Tasks](https://locu.app/api/docs#tag/tasks)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `done` | query | `string` | no | Filter tasks by completion flag Accepted values: `0`, `1`. |
| `projectId` | query | `string` | no | Filter tasks by project ID |
| `parentId` | query | `string` | no | Filter tasks by parent task ID |
| `section` | query | `string` | no | Filter tasks by section Accepted values: `0`, `1`, `2`. |
| `doneAfter` | query | `date` | no | Filter tasks completed after this timestamp |
| `doneBefore` | query | `date` | no | Filter tasks completed before this timestamp |
| `includeHtml` | query | `boolean` | no | Include description content as HTML |
| `includeMarkdown` | query | `boolean` | no | Include description content as Markdown |
| `includePlainText` | query | `boolean` | no | Include description content as plain text |
| `includeJson` | query | `boolean` | no | Include description content as structured JSON |
