# <img src="https://images.mindcloud.co/apps/icons/moorcheh-icon_1778169246402.png" alt="Moorcheh logo" width="28" height="28"> Moorcheh: Universal API

Moorcheh provides REST APIs for namespaces, semantic search, text/vector data ingestion, document retrieval, file upload URLs, deletion, and AI answer generation.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/moorcheh/latest
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://moorcheh.ai
- **Vendor API docs:** https://docs.moorcheh.ai/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Namespaces](actions/list-namespaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/list-namespaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Answer

| Action | Method | Description |
| --- | --- | --- |
| [Generate AI Answer](actions/generate-ai-answer.md) | POST | Generates an AI answer in Moorcheh from your data. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Delete Documents](actions/delete-documents.md) | DELETE | Deletes documents from a Moorcheh namespace by ID. |
| [Get Documents](actions/get-documents.md) | GET | Retrieves specific documents from a Moorcheh namespace by ID. |
| [Upload Text Data](actions/upload-text-data.md) | POST | Uploads text documents to a Moorcheh namespace. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes files from a Moorcheh namespace in storage. |

### Namespace

| Action | Method | Description |
| --- | --- | --- |
| [Create Namespace](actions/create-namespace.md) | POST | Creates a new namespace in Moorcheh. |
| [Delete Namespace](actions/delete-namespace.md) | DELETE | Deletes a namespace and its data from Moorcheh. |
| [List Namespaces](actions/list-namespaces.md) | GET | Retrieves all namespaces in your Moorcheh account. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search](actions/search.md) | GET | Finds relevant results in Moorcheh across selected namespaces. |

### Text Chunk

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Text Data](actions/fetch-text-data.md) | GET | Retrieves text chunks from a Moorcheh namespace with cursor pagination. |

### Upload Url

| Action | Method | Description |
| --- | --- | --- |
| [Get Upload File URL](actions/get-upload-file-url.md) | POST | Generates a pre-signed file upload URL in Moorcheh. |

### Vector

| Action | Method | Description |
| --- | --- | --- |
| [Delete Vectors](actions/delete-vectors.md) | DELETE | Deletes vectors from a Moorcheh namespace by ID. |
| [Upload Vector Data](actions/upload-vector-data.md) | POST | Uploads vector data to a Moorcheh namespace. |

