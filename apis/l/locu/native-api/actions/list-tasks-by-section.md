# List Tasks By Section with Locu

Retrieves tasks organized by section from Locu.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/sections`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [List Tasks By Section](https://locu.app/api/docs#tag/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `section` | query | `string` | no | Return only one section when provided Accepted values: `0`, `1`, `2`. |
| `includeHtml` | query | `boolean` | no | Include description content as HTML |
| `includeMarkdown` | query | `boolean` | no | Include description content as Markdown |
| `includePlainText` | query | `boolean` | no | Include description content as plain text |
| `includeJson` | query | `boolean` | no | Include description content as structured JSON |
