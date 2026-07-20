# Create Document Type with Docutray

## Endpoint

- **Method:** `POST`
- **Path:** `api/document-types`
- **Base URL:** `https://app.docutray.com`
- **Official documentation:** [Create Document Type](https://docs.docutray.com/docs/operations/document-types)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Document type name |
| `codeType` | body | `string` | yes | Unique code identifier |
| `description` | body | `string` | yes | Document type description |
| `jsonSchema` | body | `object` | yes | JSON Schema for document validation |
| `isDraft` | body | `boolean` | no | Whether the document type is a draft |
| `promptHints` | body | `string` | no | Hints for the OCR prompt |
| `identifyPromptHints` | body | `string` | no | Hints for the document identification prompt |
| `conversionMode` | body | `string` | no | Conversion mode |
| `keepPropertyOrdering` | body | `boolean` | no | Whether to preserve property ordering in schema |
| `isPublic` | body | `boolean` | no | Whether the document type is public |
