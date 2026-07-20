# <img src="https://images.mindcloud.co/apps/icons/typless_1776175695005.png" alt="Typless logo" width="28" height="28"> Typless: Universal API

Typless is an AI-powered document extraction platform for automating manual data entry from invoices and other documents. This app wraps the official Typless API for accounts payable workflows, document training, extraction, asynchronous polling, and pretrained-model extraction.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/typless/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://typless.com/
- **Vendor API docs:** https://typless.gitbook.io/typlessapi/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Awaiting Poll Extractions](actions/list-awaiting-poll-extractions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typless/latest/actions/list-awaiting-poll-extractions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Add Document](actions/add-document.md) | POST |  |
| [Add Document Async](actions/add-document-async.md) | POST |  |
| [Add Document Feedback](actions/add-document-feedback.md) | POST |  |
| [Extract Data](actions/extract-data.md) | POST |  |
| [Extract Data Async](actions/extract-data-async.md) | POST |  |
| [Extract Pretrained Model Data](actions/extract-pretrained-model-data.md) | POST |  |
| [Get Extraction Data](actions/get-extraction-data.md) | GET |  |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [List Awaiting Poll Extractions](actions/list-awaiting-poll-extractions.md) | GET |  |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [Start Training](actions/start-training.md) | POST |  |

