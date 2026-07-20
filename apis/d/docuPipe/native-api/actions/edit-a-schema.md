# Edit a Schema with DocuPipe

Updates a schema in DocuPipe.

## Endpoint

- **Method:** `POST`
- **Path:** `/schema/edit`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Edit a Schema](https://docs.docupipe.ai/reference/post_edit_schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schemaId` | body | `string` | yes | Unique identifier of the schema which we are editing. |
| `schemaName` | body | `string` | no | New name to assign to the schema. |
| `description` | body | `string` | no | New description to assign to the schema. |
| `guidelines` | body | `string` | no | New guidelines to assign to the schema. |
