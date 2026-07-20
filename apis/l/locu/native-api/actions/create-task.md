# Create Task with Locu

Creates a new task in Locu.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [Create Task](https://locu.app/api/docs#tag/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | Optional custom ID for the task |
| `name` | body | `string` | yes | Task name |
| `description` | body | `string` | no | Task description in markdown format |
| `parentId` | body | `string` | no | Parent task ID for subtasks |
| `projectId` | body | `string` | no | Project to assign the task to |
| `section` | body | `string` | no | Section to place the task in Accepted values: `0`, `1`, `2`. |
| `keepBreaks` | body | `boolean` | no | Preserve extra blank lines as empty paragraphs |
| `includeHtml` | query | `boolean` | no | Include description content as HTML |
| `includeMarkdown` | query | `boolean` | no | Include description content as Markdown |
| `includePlainText` | query | `boolean` | no | Include description content as plain text |
| `includeJson` | query | `boolean` | no | Include description content as structured JSON |
