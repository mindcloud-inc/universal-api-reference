# Create Template with Docupilot

Creates a template in Docupilot.

## Endpoint

- **Method:** `POST`
- **Path:** `/dashboard/api/v2/templates/`
- **Base URL:** `https://api.docupilot.app`
- **Official documentation:** [Create Template](https://help.docupilot.app/developers/templates-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `output_type` | body | `list` | yes | Accepted values: `docx`, `html`, `jpeg`, `pdf`, `png`, `pptx`, `xlsx`. |
| `title` | body | `string` | yes | — |
| `description` | body | `string` | no | — |
| `file` | body | `file` | no | — |
| `folder` | body | `number` | no | — |
| `template_gallery_id` | body | `number` | no | — |
