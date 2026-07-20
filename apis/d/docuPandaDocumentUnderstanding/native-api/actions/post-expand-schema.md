# Expand a Schema with DocuPanda - Document Understanding

Updates an existing schema with new documents in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/schema/expand`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Expand a Schema](https://docs.docupipe.ai/openapi/docupanda.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentIds` | body | `list<string>` | yes | List of document IDs to use for schema expansion. |
| `instructions` | body | `string` | no | Instructions to guide the AI when expanding the schema. |
| `schemaId` | body | `string` | yes | Unique identifier of the schema that was used with the document to make the standardization. |
