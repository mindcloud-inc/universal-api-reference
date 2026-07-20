# <img src="https://images.mindcloud.co/apps/icons/doctly_1775499585662.png" alt="Doctly logo" width="28" height="28"> Doctly: Universal API

Convert documents to Markdown and extract structured data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/doctly/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://doctly.ai
- **Vendor API docs:** https://docs.doctly.ai/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Extractors](actions/list-extractors.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doctly/latest/actions/list-extractors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Delete Document](actions/delete-document.md) | DELETE |  |
| [Get Document](actions/get-document.md) | GET |  |
| [List Documents](actions/list-documents.md) | GET |  |
| [Process Document](actions/process-document.md) | POST |  |
| [Run Extractor](actions/run-extractor.md) | POST |  |

### Extractor

| Action | Method | Description |
| --- | --- | --- |
| [Delete Extractor](actions/delete-extractor.md) | DELETE |  |
| [Get Extractor](actions/get-extractor.md) | GET |  |
| [List Extractors](actions/list-extractors.md) | GET |  |
| [Update Extractor](actions/update-extractor.md) | PUT |  |

