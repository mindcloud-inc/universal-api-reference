# Edit a Schema with DocuPanda - Document Understanding

Updates an existing schema in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/schema/edit`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Edit a Schema](https://docs.docupipe.ai/reference/post_edit_schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | New description to assign to the schema. |
| `guidelines` | body | `string` | no | New guidelines to assign to the schema. |
| `schemaId` | body | `string` | yes | Unique identifier of the schema which we are editing. |
| `schemaName` | body | `string` | no | New name to assign to the schema. |
