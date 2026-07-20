# Add a New Schema with DocuPipe

Creates a schema in DocuPipe.

## Endpoint

- **Method:** `POST`
- **Path:** `/schema`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Add a New Schema](https://docs.docupipe.ai/reference/post_schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schemaName` | body | `string` | yes | Name of the new schema. |
| `jsonSchema` | body | `object` | yes | The new JSON schema to add. Must be a valid JSON schema (https://json-schema.org/). |
| `guidelines` | body | `string` | no | Guidelines to apply to the schema to documents when standardizing. |
