# Feishu Document: Native API Reference

A consolidated summary of Feishu Document's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://open.larksuite.com/document/server-docs/docs/docs/docx-v1/document/create
- **API base URL:** `https://open.larksuite.com`

## Authentication

### Custom App Tenant Token

Use Feishu custom-app credentials to obtain a tenant access token for Docx API calls.

### Credentials

- **Client ID:** `clientId` · required · Lark custom app client ID.
- **Client Secret:** `clientSecret` · required · Lark custom app client secret.

Send these headers with each API request:

```http
Authorization: Bearer <custom.tenant_access_token>
```

[Official authentication documentation](https://open.larksuite.com/document/uAjLw4CM/ugTN1YjL4UTN24CO1UjN/trouble-shooting/how-to-choose-which-type-of-token-to-use)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | `POST /open-apis/docx/v1/documents` | [docs](https://open.larksuite.com/document/server-docs/docs/docs/docx-v1/document/create) |
| [Get Block](actions/get-block.md) | `GET /open-apis/docx/v1/documents/:document_id/blocks/:block_id` | [docs](https://open.larksuite.com/document/server-docs/docs/docs/docx-v1/document-block/get) |
| [Get Document](actions/get-document.md) | `GET /open-apis/docx/v1/documents/:document_id` | [docs](https://open.larksuite.com/document/server-docs/docs/docs/docx-v1/document/get) |
| [Get Raw Document Content](actions/get-raw-document-content.md) | `GET /open-apis/docx/v1/documents/:document_id/raw_content` | [docs](https://open.larksuite.com/document/server-docs/docs/docs/docx-v1/document/raw_content) |
| [Get Tenant Access Token](actions/get-tenant-access-token.md) | `POST /open-apis/auth/v3/tenant_access_token/internal` | [docs](https://open.larksuite.com/document/server-docs/authentication-management/access-token/tenant_access_token_internal) |
| [List Document Blocks](actions/list-document-blocks.md) | `GET /open-apis/docx/v1/documents/:document_id/blocks` | [docs](https://open.larksuite.com/document/server-docs/docs/docs/docx-v1/document-block/list) |
