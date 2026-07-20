# Get Task with Locu

Retrieves a single task by ID from Locu.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/:id`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [Get Task](https://locu.app/api/docs#tag/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Task ID |
| `includeHtml` | query | `boolean` | no | Include description content as HTML |
| `includeMarkdown` | query | `boolean` | no | Include description content as Markdown |
| `includePlainText` | query | `boolean` | no | Include description content as plain text |
| `includeJson` | query | `boolean` | no | Include description content as structured JSON |
