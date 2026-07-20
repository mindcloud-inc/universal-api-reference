# Refine a Schema with DocuPanda - Document Understanding

Updates an existing schema from feedback in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/schema/refine`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Refine a Schema](https://docs.docupipe.ai/openapi/docupanda.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | body | `string` | no | Unique identifier of the document to use for schema refinement. |
| `feedback` | body | `string` | yes | Feedback string to alter the schema. |
| `schemaId` | body | `string` | yes | Unique identifier of the schema that was used with the document to make the standardization. |
