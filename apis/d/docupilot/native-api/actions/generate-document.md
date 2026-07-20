# Generate Document with Docupilot

Generates a document from a Docupilot template.

## Endpoint

- **Method:** `POST`
- **Path:** `/dashboard/api/v2/templates/{id}/generate/`
- **Base URL:** `https://api.docupilot.app`
- **Official documentation:** [Generate Document](https://help.docupilot.app/developers/templates-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `download` | query | `list` | no | Accepted values: `false`, `file`, `true`. |
| `includeUrl` | query | `boolean` | no | — |
| `output_type` | query | `list` | no | Accepted values: `docx`, `html`, `pdf`, `png`, `pptx`, `xlsx`. |
| `payload` | body | `object` | no | Provide a JSON object that matches the documented Docupilot request body. |
