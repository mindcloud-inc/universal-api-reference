# <img src="https://images.mindcloud.co/apps/icons/vectara-icon_1775837982962.png" alt="Vectara logo" width="28" height="28"> Vectara: Universal API

Index knowledge, search data, and run grounded AI agents

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vectara/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.vectara.com
- **Vendor API docs:** https://docs.vectara.com/docs/rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Corpora](actions/list-corpora.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vectara/latest/actions/list-corpora?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Chat Completion

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion](actions/create-chat-completion.md) | GET | Creates a chat completion in Vectara. |

### Corpus

| Action | Method | Description |
| --- | --- | --- |
| [Create Corpus](actions/create-corpus.md) | POST | Creates a new corpus in Vectara. |
| [Delete Corpus](actions/delete-corpus.md) | DELETE | Deletes an existing corpus from Vectara. |
| [Get Corpus](actions/get-corpus.md) | GET | Retrieves metadata for a specific corpus from Vectara. |
| [List Corpora](actions/list-corpora.md) | GET | Retrieves a list of corpora from Vectara. |
| [Update Corpus](actions/update-corpus.md) | PUT | Updates an existing corpus in Vectara. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Add Document](actions/add-document.md) | POST | Adds a document to a Vectara corpus for indexing. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes a document from a specific Vectara corpus. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from a specific Vectara corpus. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from a specific Vectara corpus. |
| [Replace Document Metadata](actions/replace-document-metadata.md) | PUT | Replaces metadata for a document in a Vectara corpus. |
| [Update Document](actions/update-document.md) | PUT | Updates an existing document in a specific Vectara corpus. |

### Encoder

| Action | Method | Description |
| --- | --- | --- |
| [List Encoders](actions/list-encoders.md) | GET | Retrieves the available encoders from Vectara. |

### Factual Consistency Evaluation

| Action | Method | Description |
| --- | --- | --- |
| [Evaluate Factual Consistency](actions/evaluate-factual-consistency.md) | GET | Evaluates generated text for factual consistency in Vectara. |

### Generation Preset

| Action | Method | Description |
| --- | --- | --- |
| [List Generation Presets](actions/list-generation-presets.md) | GET | Retrieves available generation presets from Vectara. |

### Hallucination Correction

| Action | Method | Description |
| --- | --- | --- |
| [Correct Hallucinations](actions/correct-hallucinations.md) | GET | Corrects hallucinations in generated text with Vectara. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves background job records from Vectara. |

### Metadata Query Result

| Action | Method | Description |
| --- | --- | --- |
| [Query Metadata](actions/query-metadata.md) | GET | Queries metadata fields in a specific Vectara corpus. |

### Query Result

| Action | Method | Description |
| --- | --- | --- |
| [Advanced Single Corpus Query](actions/advanced-single-corpus-query.md) | GET | Retrieves advanced query results from a specific Vectara corpus. |
| [Multi Corpora Query](actions/multi-corpora-query.md) | GET | Retrieves query results across multiple Vectara corpora. |
| [Simple Single Corpus Query](actions/simple-single-corpus-query.md) | GET | Retrieves query results from a specific Vectara corpus. |

### Reranker

| Action | Method | Description |
| --- | --- | --- |
| [List Rerankers](actions/list-rerankers.md) | GET | Retrieves the available rerankers from Vectara. |

### Upload

| Action | Method | Description |
| --- | --- | --- |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to a Vectara corpus for indexing. |

