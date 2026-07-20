# FlowiseAI: Native API Reference

A consolidated summary of FlowiseAI's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.flowiseai.com/api-reference
- **API base URL:** `https://cloud.flowiseai.com/api/v1`

## Authentication

### API Key

Flowise Cloud API key. Send as Bearer authentication for Flowise REST API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.flowiseai.com/api-reference/chatflows)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Attachment Array](actions/create-attachment-array.md) | `POST /attachments/{chatflowId}/{chatId}` | [docs](https://docs.flowiseai.com/api-reference/attachments) |
| [Create Chatflow](actions/create-chatflow.md) | `POST /chatflows` | [docs](https://docs.flowiseai.com/api-reference/chatflows) |
| [Create Document Store](actions/create-document-store.md) | `POST /document-store/store` | [docs](https://docs.flowiseai.com/api-reference/document-store) |
| [Create Tool](actions/create-tool.md) | `POST /tools` | [docs](https://docs.flowiseai.com/api-reference/tools) |
| [Create Variable](actions/create-variable.md) | `POST /variables` | [docs](https://docs.flowiseai.com/api-reference/variables) |
| [Delete Chatflow](actions/delete-chatflow.md) | `DELETE /chatflows/{id}` | [docs](https://docs.flowiseai.com/api-reference/chatflows) |
| [Delete Document Store](actions/delete-document-store.md) | `DELETE /document-store/store/{id}` | [docs](https://docs.flowiseai.com/api-reference/document-store) |
| [Delete Document Store Chunk](actions/delete-document-store-chunk.md) | `DELETE /document-store/chunks/{storeId}/{loaderId}/{chunkId}` | [docs](https://docs.flowiseai.com/api-reference/document-store) |
| [Delete Document Store Loader](actions/delete-document-store-loader.md) | `DELETE /document-store/loader/{storeId}/{loaderId}` | [docs](https://docs.flowiseai.com/api-reference/document-store) |
| [Delete Document Store Vector Store](actions/delete-document-store-vector-store.md) | `DELETE /document-store/vectorstore/{id}` | [docs](https://docs.flowiseai.com/api-reference/document-store) |
| [Delete Tool](actions/delete-tool.md) | `DELETE /tools/{id}` | [docs](https://docs.flowiseai.com/api-reference/tools) |
| [Delete Variable](actions/delete-variable.md) | `DELETE /variables/{id}` | [docs](https://docs.flowiseai.com/api-reference/variables) |
| [Get Chatflow](actions/get-chatflow.md) | `GET /chatflows/{id}` | [docs](https://docs.flowiseai.com/api-reference/chatflows) |
| [Get Chatflow by API Key](actions/get-chatflow-by-api-key.md) | `GET /chatflows/apikey/{apikey}` | [docs](https://docs.flowiseai.com/api-reference/chatflows) |
| [Get Document Store](actions/get-document-store.md) | `GET /document-store/store/{id}` | [docs](https://docs.flowiseai.com/api-reference/document-store) |
| [Get Tool](actions/get-tool.md) | `GET /tools/{id}` | [docs](https://docs.flowiseai.com/api-reference/tools) |
| [List Chatflows](actions/list-chatflows.md) | `GET /chatflows` | [docs](https://docs.flowiseai.com/api-reference/chatflows) |
| [List Document Store Chunks](actions/list-document-store-chunks.md) | `GET /document-store/chunks/{storeId}/{loaderId}/{pageNo}` | [docs](https://docs.flowiseai.com/api-reference/document-store) |
| [List Document Stores](actions/list-document-stores.md) | `GET /document-store/store` | [docs](https://docs.flowiseai.com/api-reference/document-store) |
| [List Tools](actions/list-tools.md) | `GET /tools` | [docs](https://docs.flowiseai.com/api-reference/tools) |
| [List Variables](actions/list-variables.md) | `GET /variables` | [docs](https://docs.flowiseai.com/api-reference/variables) |
| [Ping Flowise API](actions/ping-flowise-api.md) | `GET /ping` | [docs](https://docs.flowiseai.com/api-reference/ping) |
| [Query Document Store Vector Store](actions/query-document-store-vector-store.md) | `POST /document-store/vectorstore/query` | [docs](https://docs.flowiseai.com/api-reference/document-store) |
| [Refresh Document Store](actions/refresh-document-store.md) | `POST /document-store/refresh/{id}` | [docs](https://docs.flowiseai.com/api-reference/document-store) |
| [Update Chatflow](actions/update-chatflow.md) | `PUT /chatflows/{id}` | [docs](https://docs.flowiseai.com/api-reference/chatflows) |
| [Update Document Store](actions/update-document-store.md) | `PUT /document-store/store/{id}` | [docs](https://docs.flowiseai.com/api-reference/document-store) |
| [Update Document Store Chunk](actions/update-document-store-chunk.md) | `PUT /document-store/chunks/{storeId}/{loaderId}/{chunkId}` | [docs](https://docs.flowiseai.com/api-reference/document-store) |
| [Update Tool](actions/update-tool.md) | `PUT /tools/{id}` | [docs](https://docs.flowiseai.com/api-reference/tools) |
| [Update Variable](actions/update-variable.md) | `PUT /variables/{id}` | [docs](https://docs.flowiseai.com/api-reference/variables) |
| [Upsert Document Store](actions/upsert-document-store.md) | `POST /document-store/upsert/{id}` | [docs](https://docs.flowiseai.com/api-reference/document-store) |
