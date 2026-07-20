# Bulk Upload Knowledge Base Documents with Docutray

## Endpoint

- **Method:** `POST`
- **Path:** `api/knowledge-bases/:id/documents/bulk-upload`
- **Base URL:** `https://app.docutray.com`
- **Official documentation:** [Bulk Upload Knowledge Base Documents](https://docs.docutray.com/docs/operations/knowledge-bases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of the Knowledge Base |
| `documents[]` | body | `array<object>` | yes | List of documents to upload |
