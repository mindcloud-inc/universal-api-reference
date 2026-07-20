# Upload Text Data with Moorcheh

Uploads text documents to a Moorcheh namespace.

## Endpoint

- **Method:** `POST`
- **Path:** `/namespaces/:namespace_name/documents`
- **Base URL:** `https://api.moorcheh.ai/v1`
- **Official documentation:** [Upload Text Data](https://docs.moorcheh.ai/api-reference/data/upload-text)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `namespace_name` | path | `string` | yes | Name of the text namespace to upload documents to. |
| `documents[]` | body | `array<object>` | yes | Array of flat document objects with id, text, and optional metadata fields. |
