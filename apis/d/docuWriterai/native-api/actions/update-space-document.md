# Update Space Document with DocuWriter.ai

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/spaces/{{space}}/documents/{{spaceMenuItem}}`
- **Base URL:** `https://app.docuwriter.ai`
- **Official documentation:** [Update Space Document](https://docs.docuwriter.ai/docuwriterai-api-docs/92059)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | no | New document body content. |
| `parent_id` | body | `number` | no | Optional parent folder ID. |
| `space` | path | `string` | yes | ID or UUID of the Space. |
| `spaceMenuItem` | path | `number` | yes | ID of the document to update. |
| `title` | body | `string` | no | New document title. |
| `type` | body | `string` | no | Storage format: blank or markdown. |
