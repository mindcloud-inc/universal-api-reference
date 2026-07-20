# Create Project with Locu

Creates a new project in Locu.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [Create Project](https://locu.app/api/docs#tag/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | Optional custom ID for the project |
| `name` | body | `string` | yes | Name of the project |
| `description` | body | `string` | no | Project description in markdown format |
| `icon` | body | `string` | no | Project icon as a Lucide icon name or emoji shortcode |
| `color` | body | `string` | no | Hex color for the icon |
| `keepBreaks` | body | `boolean` | no | Preserve extra blank lines as empty paragraphs |
| `includeHtml` | query | `boolean` | no | Include description content as HTML |
| `includeMarkdown` | query | `boolean` | no | Include description content as Markdown |
| `includePlainText` | query | `boolean` | no | Include description content as plain text |
| `includeJson` | query | `boolean` | no | Include description content as structured JSON |
