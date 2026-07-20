# Frappe: Native API Reference

A consolidated summary of Frappe's API configuration and 46 documented operations, with links to official documentation.

- **Official docs:** https://docs.frappe.io/framework/user/en/guides/integration/rest_api
- **API base URL:** `{siteUrl}`

## Authentication

### Frappe Token Auth

Use a Frappe site URL plus API key and API secret. Requests send Authorization: token <api_key>:<api_secret>.

### Credentials

- **Site URL:** `siteUrl` · required · Enter the full HTTPS base URL of your Frappe site. Include the scheme and do not add a trailing /api path.
- **API Key:** `apiKey` · required · The API key generated on the Frappe user record.
- **API Secret:** `apiSecret` · required · The API secret generated with the Frappe API key.

[Official authentication documentation](https://docs.frappe.io/framework/v15/user/en/guides/integration/rest_api/token_based_authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit_page_length` in the query string to set the page size (default 20; accepted range 1–1000). Use `limit_start` in the query string as the record offset; numbering starts at 0.

## Endpoints (46 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Comment To Document V2](actions/add-comment-to-document-v2.md) | `POST /api/v2/document/{{arguments.doctype}}/{{arguments.documentName}}/method/add_comment` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Call DocType Controller Method V2 (GET)](actions/call-doctype-controller-method-v2-get.md) | `GET /api/v2/method/{{arguments.doctype}}/{{arguments.methodName}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Call DocType Controller Method V2 (POST)](actions/call-doctype-controller-method-v2-post.md) | `POST /api/v2/method/{{arguments.doctype}}/{{arguments.methodName}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Call Whitelisted Method V1 Alias (GET)](actions/call-whitelisted-method-v1-alias-get.md) | `GET /api/v1/method/{{arguments.methodPath}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Call Whitelisted Method V1 Alias (POST)](actions/call-whitelisted-method-v1-alias-post.md) | `POST /api/v1/method/{{arguments.methodPath}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Call Whitelisted Method V1 (GET)](actions/call-whitelisted-method-v1-get.md) | `GET /api/method/{{arguments.methodPath}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Call Whitelisted Method V1 (POST)](actions/call-whitelisted-method-v1-post.md) | `POST /api/method/{{arguments.methodPath}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Call Whitelisted Method V2 (GET)](actions/call-whitelisted-method-v2-get.md) | `GET /api/v2/method/{{arguments.methodPath}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Call Whitelisted Method V2 (POST)](actions/call-whitelisted-method-v2-post.md) | `POST /api/v2/method/{{arguments.methodPath}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Cancel Document V2](actions/cancel-document-v2.md) | `POST /api/v2/document/{{arguments.doctype}}/{{arguments.documentName}}/method/cancel` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Copy Document V2](actions/copy-document-v2.md) | `GET /api/v2/document/{{arguments.doctype}}/{{arguments.documentName}}/copy` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Create Document V1](actions/create-document-v1.md) | `POST /api/resource/{{arguments.doctype}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api/manipulating_documents) |
| [Create Document V1 Alias](actions/create-document-v1-alias.md) | `POST /api/v1/resource/{{arguments.doctype}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Create Document V2](actions/create-document-v2.md) | `POST /api/v2/document/{{arguments.doctype}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Delete Document V1](actions/delete-document-v1.md) | `DELETE /api/resource/{{arguments.doctype}}/{{arguments.documentName}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api/manipulating_documents) |
| [Delete Document V1 Alias](actions/delete-document-v1-alias.md) | `DELETE /api/v1/resource/{{arguments.doctype}}/{{arguments.documentName}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Delete Document V2](actions/delete-document-v2.md) | `DELETE /api/v2/document/{{arguments.doctype}}/{{arguments.documentName}}/` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Get DocType Count V2](actions/get-doctype-count-v2.md) | `GET /api/v2/doctype/{{arguments.doctype}}/count` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Get DocType Metadata V2](actions/get-doctype-metadata-v2.md) | `GET /api/v2/doctype/{{arguments.doctype}}/meta` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Get Document V1](actions/get-document-v1.md) | `GET /api/resource/{{arguments.doctype}}/{{arguments.documentName}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api/manipulating_documents) |
| [Get Document V1 Alias](actions/get-document-v1-alias.md) | `GET /api/v1/resource/{{arguments.doctype}}/{{arguments.documentName}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Get Document V2](actions/get-document-v2.md) | `GET /api/v2/document/{{arguments.doctype}}/{{arguments.documentName}}/` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Get Logged User](actions/get-logged-user.md) | `GET /api/method/frappe.auth.get_logged_user` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Get Logged User V1 Alias](actions/get-logged-user-v1-alias.md) | `GET /api/v1/method/frappe.auth.get_logged_user` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [List Documents V1](actions/list-documents-v1.md) | `GET /api/resource/{{arguments.doctype}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api/listing_documents) |
| [List Documents V1 Alias](actions/list-documents-v1-alias.md) | `GET /api/v1/resource/{{arguments.doctype}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [List Documents V2](actions/list-documents-v2.md) | `GET /api/v2/document/{{arguments.doctype}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Login V1](actions/login-v1.md) | `POST /api/method/login` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api/simple_authentication) |
| [Login V1 Alias](actions/login-v1-alias.md) | `POST /api/v1/method/login` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api/simple_authentication) |
| [Login V2](actions/login-v2.md) | `POST /api/v2/method/login` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Logout V1](actions/logout-v1.md) | `GET /api/method/logout` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api/simple_authentication) |
| [Logout V1 Alias](actions/logout-v1-alias.md) | `GET /api/v1/method/logout` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api/simple_authentication) |
| [Logout V2](actions/logout-v2.md) | `POST /api/v2/method/logout` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Patch Document V2](actions/patch-document-v2.md) | `PATCH /api/v2/document/{{arguments.doctype}}/{{arguments.documentName}}/` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Ping Site V2](actions/ping-site-v2.md) | `GET /api/v2/method/ping` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Put Document V2](actions/put-document-v2.md) | `PUT /api/v2/document/{{arguments.doctype}}/{{arguments.documentName}}/` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Rename Document V2](actions/rename-document-v2.md) | `POST /api/v2/document/{{arguments.doctype}}/{{arguments.documentName}}/method/rename` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Run Doc Method RPC V2](actions/run-doc-method-rpc-v2.md) | `POST /api/v2/method/run_doc_method` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Run Document Method V2 (GET)](actions/run-document-method-v2-get.md) | `GET /api/v2/document/{{arguments.doctype}}/{{arguments.documentName}}/method/{{arguments.methodName}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Run Document Method V2 (POST)](actions/run-document-method-v2-post.md) | `POST /api/v2/document/{{arguments.doctype}}/{{arguments.documentName}}/method/{{arguments.methodName}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Submit Document V2](actions/submit-document-v2.md) | `POST /api/v2/document/{{arguments.doctype}}/{{arguments.documentName}}/method/submit` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Update Document V1](actions/update-document-v1.md) | `PUT /api/resource/{{arguments.doctype}}/{{arguments.documentName}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api/manipulating_documents) |
| [Update Document V1 Alias](actions/update-document-v1-alias.md) | `PUT /api/v1/resource/{{arguments.doctype}}/{{arguments.documentName}}` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
| [Upload File V1](actions/upload-file-v1.md) | `POST /api/method/upload_file` | [docs](https://docs.frappe.io/framework/user/en/api/rest) |
| [Upload File V1 Alias](actions/upload-file-v1-alias.md) | `POST /api/v1/method/upload_file` | [docs](https://docs.frappe.io/framework/user/en/api/rest) |
| [Upload File V2](actions/upload-file-v2.md) | `POST /api/v2/method/upload_file` | [docs](https://docs.frappe.io/framework/user/en/guides/integration/rest_api) |
