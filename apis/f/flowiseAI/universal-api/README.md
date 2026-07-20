# <img src="https://images.mindcloud.co/apps/icons/128289781_1776795008941.png" alt="FlowiseAI logo" width="28" height="28"> FlowiseAI: Universal API

FlowiseAI is an open-source visual platform for building and operating LLM apps, agents, chatflows, tools, document stores, and prediction APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/flowiseAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://flowiseai.com/
- **Vendor API docs:** https://docs.flowiseai.com/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Chatflows](actions/list-chatflows.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/list-chatflows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Create Attachment Array](actions/create-attachment-array.md) | POST | Creates an attachment array for a FlowiseAI chat. |

### Chatflow

| Action | Method | Description |
| --- | --- | --- |
| [Create Chatflow](actions/create-chatflow.md) | POST | Creates a new chatflow in FlowiseAI. |
| [Delete Chatflow](actions/delete-chatflow.md) | DELETE | Deletes an existing chatflow from FlowiseAI. |
| [Get Chatflow](actions/get-chatflow.md) | GET | Retrieves a specific chatflow from FlowiseAI. |
| [Get Chatflow by API Key](actions/get-chatflow-by-api-key.md) | GET | Retrieves a FlowiseAI chatflow by API key. |
| [List Chatflows](actions/list-chatflows.md) | GET | Retrieves a list of chatflows from FlowiseAI. |
| [Update Chatflow](actions/update-chatflow.md) | PUT | Updates an existing chatflow in FlowiseAI. |

### Document Store

| Action | Method | Description |
| --- | --- | --- |
| [Create Document Store](actions/create-document-store.md) | POST | Creates a new document store in FlowiseAI. |
| [Delete Document Store](actions/delete-document-store.md) | DELETE | Deletes an existing document store from FlowiseAI. |
| [Get Document Store](actions/get-document-store.md) | GET | Retrieves a specific document store from FlowiseAI. |
| [List Document Stores](actions/list-document-stores.md) | GET | Retrieves all document stores from FlowiseAI. |
| [Refresh Document Store](actions/refresh-document-store.md) | PUT | Reprocesses all documents in a FlowiseAI document store. |
| [Update Document Store](actions/update-document-store.md) | PUT | Updates an existing document store in FlowiseAI. |
| [Upsert Document Store](actions/upsert-document-store.md) | PUT | Upserts documents in a FlowiseAI document store. |

### Document Store Chunk

| Action | Method | Description |
| --- | --- | --- |
| [Delete Document Store Chunk](actions/delete-document-store-chunk.md) | DELETE | Deletes a specific document chunk from FlowiseAI. |
| [List Document Store Chunks](actions/list-document-store-chunks.md) | GET | Retrieves chunks from a FlowiseAI document loader. |
| [Update Document Store Chunk](actions/update-document-store-chunk.md) | PUT | Updates a specific document chunk in FlowiseAI. |

### Document Store Loader

| Action | Method | Description |
| --- | --- | --- |
| [Delete Document Store Loader](actions/delete-document-store-loader.md) | DELETE | Deletes a document loader and chunks from FlowiseAI. |

### Document Store Vector Query

| Action | Method | Description |
| --- | --- | --- |
| [Query Document Store Vector Store](actions/query-document-store-vector-store.md) | GET | Queries a FlowiseAI document store vector store. |

### Document Store Vector Store

| Action | Method | Description |
| --- | --- | --- |
| [Delete Document Store Vector Store](actions/delete-document-store-vector-store.md) | DELETE | Deletes vector store data from a FlowiseAI document store. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Ping Flowise API](actions/ping-flowise-api.md) | GET | Checks whether the FlowiseAI server is running. |

### Tool

| Action | Method | Description |
| --- | --- | --- |
| [Create Tool](actions/create-tool.md) | POST | Creates a new tool in FlowiseAI. |
| [Delete Tool](actions/delete-tool.md) | DELETE | Deletes an existing tool from FlowiseAI. |
| [Get Tool](actions/get-tool.md) | GET | Retrieves a specific tool from FlowiseAI. |
| [List Tools](actions/list-tools.md) | GET | Retrieves a list of tools from FlowiseAI. |
| [Update Tool](actions/update-tool.md) | PUT | Updates an existing tool in FlowiseAI. |

### Variable

| Action | Method | Description |
| --- | --- | --- |
| [Create Variable](actions/create-variable.md) | POST | Creates a new variable in FlowiseAI. |
| [Delete Variable](actions/delete-variable.md) | DELETE | Deletes an existing variable from FlowiseAI. |
| [List Variables](actions/list-variables.md) | GET | Retrieves a list of variables from FlowiseAI. |
| [Update Variable](actions/update-variable.md) | PUT | Updates an existing variable in FlowiseAI. |

