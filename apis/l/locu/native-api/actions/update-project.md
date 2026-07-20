# Update Project with Locu

Updates an existing project in Locu.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:id`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [Update Project](https://locu.app/api/docs#tag/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Project ID |
| `name` | body | `string` | no | New name for the project |
| `description` | body | `string` | no | Project description in markdown format |
| `icon` | body | `string` | no | New icon for the project |
| `color` | body | `string` | no | New hex color for the icon |
| `state` | body | `string` | no | New state for the project Accepted values: `0`, `1`. |
| `keepBreaks` | body | `boolean` | no | Preserve extra blank lines as empty paragraphs |
| `includeHtml` | query | `boolean` | no | Include description content as HTML |
| `includeMarkdown` | query | `boolean` | no | Include description content as Markdown |
| `includePlainText` | query | `boolean` | no | Include description content as plain text |
| `includeJson` | query | `boolean` | no | Include description content as structured JSON |
