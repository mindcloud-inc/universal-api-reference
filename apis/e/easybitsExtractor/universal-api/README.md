# <img src="https://images.mindcloud.co/apps/icons/easybits-extractor_1776088154020.png" alt="easybits Extractor logo" width="28" height="28"> easybits Extractor: Universal API

Integration-ready data extraction pipelines for n8n workflows and API-based document processing.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/easybitsExtractor/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://extractor.easybits.tech/
- **Vendor API docs:** https://extractor.easybits.tech/documentation/integration

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Pipeline Connection](actions/verify-pipeline-connection.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easybitsExtractor/latest/actions/verify-pipeline-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Extracted Data

| Action | Method | Description |
| --- | --- | --- |
| [Extract Data](actions/extract-data.md) | GET | Extracts structured data from documents in easybits Extractor. |

### Pipeline Connection Status

| Action | Method | Description |
| --- | --- | --- |
| [Verify Pipeline Connection](actions/verify-pipeline-connection.md) | GET | Verifies a pipeline connection in easybits Extractor. |

