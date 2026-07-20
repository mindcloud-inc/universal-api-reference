# <img src="https://images.mindcloud.co/apps/icons/feishu-document_1776187446252.png" alt="Feishu Document logo" width="28" height="28"> Feishu Document: Universal API

Build, read, and inspect Feishu documents through the Lark Open Platform Docx API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/feishuDocument/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://open.larksuite.com
- **Vendor API docs:** https://open.larksuite.com/document/server-docs/docs/docs/docx-v1/document/create

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Block](actions/get-block.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feishuDocument/latest/actions/get-block?connectionId=$CONNECTION_ID&blockId=string&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Tenant Access Token](actions/get-tenant-access-token.md) | POST | Retrieves a tenant access token from Feishu. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a new document in Feishu Docs. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get Document](actions/get-document.md) | GET | Retrieves document details from Feishu Docs. |
| [Get Raw Document Content](actions/get-raw-document-content.md) | GET | Retrieves raw text content from a Feishu document. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Block](actions/get-block.md) | GET | Retrieves a specific block from a Feishu document. |
| [List Document Blocks](actions/list-document-blocks.md) | GET | Retrieves all blocks from a Feishu document. |

