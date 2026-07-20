# List Document Blocks with Feishu Document

Retrieves all blocks from a Feishu document.

## Endpoint

- **Method:** `GET`
- **Path:** `/open-apis/docx/v1/documents/:document_id/blocks`
- **Base URL:** `https://open.larksuite.com`
- **Official documentation:** [List Document Blocks](https://open.larksuite.com/document/server-docs/docs/docs/docx-v1/document-block/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The unique document token. |
