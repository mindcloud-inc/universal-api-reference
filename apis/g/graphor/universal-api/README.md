# <img src="https://images.mindcloud.co/apps/icons/graphor_1775824524782.png" alt="Graphor logo" width="28" height="28"> Graphor: Universal API

Graphor ingests documents, chats over indexed content, and extracts structured data through hosted retrieval and extraction APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/graphor/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.graphorlm.com
- **Vendor API docs:** https://docs.graphorlm.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sources](actions/list-sources.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/graphor/latest/actions/list-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Builds

| Action | Method | Description |
| --- | --- | --- |
| [Get Build Status](actions/get-build-status.md) | GET | Retrieves source build status from Graphor by build ID. |
| [Get Build Status With Elements](actions/get-build-status-with-elements.md) | GET | Retrieves source build status and elements from Graphor. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Ask Documents](actions/ask-documents.md) | GET | Retrieves answers about your documents from Graphor. |
| [Ask Documents With Structured Output](actions/ask-documents-with-structured-output.md) | GET | Retrieves structured answers about your documents from Graphor. |
| [Continue Document Conversation](actions/continue-document-conversation.md) | GET | Retrieves follow-up answers from Graphor with conversation memory. |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [Crawl URL Sources](actions/crawl-url-sources.md) | POST | Creates a new source in Graphor by crawling a URL. |
| [Delete Source](actions/delete-source.md) | DELETE | Deletes an existing source from Graphor by file ID. |
| [Ingest File](actions/ingest-file.md) | POST | Creates a new source in Graphor from a file. |
| [Ingest GitHub Repository](actions/ingest-github-repository.md) | POST | Creates a new source in Graphor from a GitHub repository. |
| [Ingest URL](actions/ingest-url.md) | POST | Creates a new source in Graphor from a URL. |
| [Ingest YouTube Video](actions/ingest-youtube-video.md) | POST | Creates a new source in Graphor from a YouTube video. |
| [List Sources](actions/list-sources.md) | GET | Retrieves sources from your Graphor project. |
| [List Sources By File ID](actions/list-sources-by-file-id.md) | GET | Finds sources in Graphor by file ID. |
| [Reprocess Source](actions/reprocess-source.md) | PUT | Updates an existing source in Graphor with a new partition method. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Source Elements](actions/get-source-elements.md) | GET | Retrieves parsed source elements from Graphor by file ID. |
| [Get Source Elements By Type](actions/get-source-elements-by-type.md) | GET | Retrieves parsed source elements from Graphor by element type. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Extract Structured Data](actions/extract-structured-data.md) | POST | Extracts structured data from Graphor documents. |
| [Extract Structured Data By File Name](actions/extract-structured-data-by-file-name.md) | POST | Extracts structured data from Graphor documents by file name. |
| [Retrieve Relevant Chunks](actions/retrieve-relevant-chunks.md) | GET | Retrieves relevant document chunks from Graphor by semantic search. |
| [Retrieve Relevant Chunks By File Name](actions/retrieve-relevant-chunks-by-file-name.md) | GET | Retrieves relevant document chunks from Graphor by file name. |

