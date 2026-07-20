# Get Project with Locu

Retrieves a single project by ID from Locu.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:id`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [Get Project](https://locu.app/api/docs#tag/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Project ID |
| `includeHtml` | query | `boolean` | no | Include description content as HTML |
| `includeMarkdown` | query | `boolean` | no | Include description content as Markdown |
| `includePlainText` | query | `boolean` | no | Include description content as plain text |
| `includeJson` | query | `boolean` | no | Include description content as structured JSON |
