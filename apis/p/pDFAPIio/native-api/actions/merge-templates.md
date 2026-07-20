# Merge Templates with PDF-API.io

Creates one PDF document from multiple templates in PDF-API.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates/merge`
- **Base URL:** `https://pdf-api.io/api`
- **Official documentation:** [Merge Templates](https://pdf-api.io/en/docs/api/merge-templates)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templates[]` | body | `array<object>` | yes | The ordered list of templates to merge into a single PDF. |
| `templates[].id` | body | `list<number>` | yes | The identifier of the template to merge. |
| `templates[].data` | body | `object` | yes | Key-value pairs representing the data to replace in that template before merging. |
| `output` | body | `list<string>` | no | Optional output format for the merged PDF response. Accepted values: `pdf`, `url`. |
