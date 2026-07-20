# Update Template with Docupilot

Updates an existing template in Docupilot.

## Endpoint

- **Method:** `PUT`
- **Path:** `/dashboard/api/v2/templates/{id}/`
- **Base URL:** `https://api.docupilot.app`
- **Official documentation:** [Update Template](https://help.docupilot.app/developers/templates-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `preferences.info` | body | `object` | yes | — |
| `folder.name` | body | `string` | yes | — |
| `title` | body | `string` | yes | — |
| `preferences.auto_number` | body | `number` | no | — |
| `description` | body | `string` | no | — |
| `document_status` | body | `list` | no | Accepted values: `active`, `test`. |
| `preferences.dynamic_images[]` | body | `array<object>` | no | — |
| `preferences.emulate_mode` | body | `list` | no | Accepted values: ``, `print`, `screen`. |
| `preferences.flatten_pdf` | body | `boolean` | no | — |
| `preferences.footer` | body | `string` | no | — |
| `preferences.format` | body | `list` | no | Accepted values: `A3`, `A4`, `A5`, `Custom`, `Legal`, `Letter`, `Tabloid`. |
| `preferences.header` | body | `string` | no | — |
| `preferences.height` | body | `number` | no | — |
| `preferences.margin` | body | `object` | no | — |
| `preferences.orientation` | body | `list` | no | Accepted values: `landscape`, `portrait`. |
| `preferences.output_file_name` | body | `string` | no | — |
| `preferences.output_type` | body | `list` | no | Accepted values: `docx`, `html`, `jpeg`, `pdf`, `png`, `pptx`, `xlsx`. |
| `preferences.password` | body | `string` | no | — |
| `preferences.timezone` | body | `string` | no | — |
| `preferences.width` | body | `number` | no | — |
