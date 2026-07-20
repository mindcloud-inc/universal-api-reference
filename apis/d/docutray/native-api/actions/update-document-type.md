# Update Document Type with Docutray

## Endpoint

- **Method:** `PUT`
- **Path:** `api/document-types/:id`
- **Base URL:** `https://app.docutray.com`
- **Official documentation:** [Update Document Type](https://docs.docutray.com/docs/operations/document-types)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Document type ID |
| `name` | body | `string` | no | Document type name |
| `description` | body | `string` | no | Document type description |
| `jsonSchema` | body | `object` | no | JSON Schema for document validation |
| `isDraft` | body | `boolean` | no | Whether the document type is a draft |
| `promptHints` | body | `string` | no | Hints for the OCR prompt |
| `identifyPromptHints` | body | `string` | no | Hints for the document identification prompt |
| `conversionMode` | body | `string` | no | Conversion mode |
| `keepPropertyOrdering` | body | `boolean` | no | Whether to preserve property ordering in schema |
| `isPublic` | body | `boolean` | no | Whether the document type is public |
