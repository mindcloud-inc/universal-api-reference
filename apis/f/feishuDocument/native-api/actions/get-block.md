# Get Block with Feishu Document

Retrieves a specific block from a Feishu document.

## Endpoint

- **Method:** `GET`
- **Path:** `/open-apis/docx/v1/documents/:document_id/blocks/:block_id`
- **Base URL:** `https://open.larksuite.com`
- **Official documentation:** [Get Block](https://open.larksuite.com/document/server-docs/docs/docs/docx-v1/document-block/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `block_id` | path | `string` | yes | The unique block id within the document. |
| `document_id` | path | `string` | yes | The unique document token. |
