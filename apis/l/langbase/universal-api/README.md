# <img src="https://images.mindcloud.co/apps/icons/langbase_1776191584524.png" alt="Langbase logo" width="28" height="28"> Langbase: Universal API

Build, run, and trace AI pipes, memory, threads, and tools

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/langbase/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://langbase.com
- **Vendor API docs:** https://langbase.com/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langbase/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Agent Run

| Action | Method | Description |
| --- | --- | --- |
| [Run Agent](actions/run-agent.md) | POST |  |

### Chunking Result

| Action | Method | Description |
| --- | --- | --- |
| [Chunk Content](actions/chunk-content.md) | POST |  |

### Crawl Result

| Action | Method | Description |
| --- | --- | --- |
| [Crawl Web Pages](actions/crawl-web-pages.md) | GET |  |

### Embedding Result

| Action | Method | Description |
| --- | --- | --- |
| [Generate Embeddings](actions/generate-embeddings.md) | POST |  |

### Image Generation

| Action | Method | Description |
| --- | --- | --- |
| [Generate Images](actions/generate-images.md) | POST |  |

### Memory

| Action | Method | Description |
| --- | --- | --- |
| [Create Memory](actions/create-memory.md) | POST |  |
| [Delete Memory](actions/delete-memory.md) | DELETE |  |
| [List Memories](actions/list-memories.md) | GET |  |

### Memory Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Memory Document Upload URL](actions/create-memory-document-upload-url.md) | POST |  |
| [Delete Memory Document](actions/delete-memory-document.md) | DELETE |  |
| [List Memory Documents](actions/list-memory-documents.md) | GET |  |
| [Retry Memory Document Embeddings](actions/retry-memory-document-embeddings.md) | PUT |  |

### Memory Retrieval

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Memory Chunks](actions/retrieve-memory-chunks.md) | GET |  |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET |  |

### Parsed Document

| Action | Method | Description |
| --- | --- | --- |
| [Parse Document](actions/parse-document.md) | POST |  |

### Pipe

| Action | Method | Description |
| --- | --- | --- |
| [Create Pipe](actions/create-pipe.md) | POST |  |
| [Get Pipe](actions/get-pipe.md) | GET |  |
| [List Pipes](actions/list-pipes.md) | GET |  |
| [Run Pipe](actions/run-pipe.md) | POST |  |
| [Update Pipe](actions/update-pipe.md) | PUT |  |

### Thread

| Action | Method | Description |
| --- | --- | --- |
| [Create Thread](actions/create-thread.md) | POST |  |
| [Delete Thread](actions/delete-thread.md) | DELETE |  |
| [Get Thread](actions/get-thread.md) | GET |  |
| [Update Thread](actions/update-thread.md) | PUT |  |

### Thread Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Thread Messages](actions/create-thread-messages.md) | POST |  |
| [Delete Thread Message](actions/delete-thread-message.md) | DELETE |  |
| [List Thread Messages](actions/list-thread-messages.md) | GET |  |
| [Update Thread Message](actions/update-thread-message.md) | PUT |  |

### Trace

| Action | Method | Description |
| --- | --- | --- |
| [Get Trace](actions/get-trace.md) | GET |  |
| [List Traces](actions/list-traces.md) | GET |  |

### Web Search

| Action | Method | Description |
| --- | --- | --- |
| [Search Web](actions/search-web.md) | GET |  |

