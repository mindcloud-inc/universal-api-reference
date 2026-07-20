# Update a Schema with DocuPanda - Document Understanding

Updates a schema by creating a new version in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/schema/update`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Update a Schema](https://docs.docupipe.ai/openapi/docupanda.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jsonSchema` | body | `object` | no | The new JSON schema to update. Must be a valid JSON schema (https://json-schema.org/). If not provided, the existing JSON schema will be used. |
| `schemaId` | body | `string` | yes | Unique identifier of the schema which we are updating. |
| `schemaName` | body | `string` | yes | Name of the new schema. |
