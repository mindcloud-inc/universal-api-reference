# Update Task with Locu

Updates an existing task in Locu.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tasks/:id`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [Update Task](https://locu.app/api/docs#tag/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Task ID |
| `name` | body | `string` | no | Task name |
| `description` | body | `string` | no | Task description in markdown format |
| `done` | body | `string` | no | Set task completion state Accepted values: `0`, `1`. |
| `projectId` | body | `string` | no | Project to assign the task to |
| `waiting.reason` | body | `string` | no | Reason for marking the task as waiting |
| `keepBreaks` | body | `boolean` | no | Preserve extra blank lines as empty paragraphs |
| `includeHtml` | query | `boolean` | no | Include description content as HTML |
| `includeMarkdown` | query | `boolean` | no | Include description content as Markdown |
| `includePlainText` | query | `boolean` | no | Include description content as plain text |
| `includeJson` | query | `boolean` | no | Include description content as structured JSON |
