# <img src="https://images.mindcloud.co/apps/icons/l-lmwhisperer_1775758364271.png" alt="LLMWhisperer logo" width="28" height="28"> LLMWhisperer: Universal API

LLMWhisperer extracts text and document structure from PDFs, scans, images, Office files, and spreadsheets for downstream LLM and automation workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lLMWhisperer/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://llmwhisperer.unstract.com/
- **Vendor API docs:** https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_text_extraction_api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Usage Metrics](actions/get-usage-metrics.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/get-usage-metrics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage Metrics](actions/get-usage-metrics.md) | GET | Retrieves account usage metrics from LLMWhisperer. |
| [Get Usage Stats](actions/get-usage-stats.md) | GET | Retrieves tagged usage statistics from LLMWhisperer. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Get Extraction Details](actions/get-extraction-details.md) | GET | Retrieves details for an LLMWhisperer extraction job. |
| [Get Extraction Status](actions/get-extraction-status.md) | GET | Retrieves the status of an LLMWhisperer extraction job. |
| [Get Highlight Lines](actions/get-highlight-lines.md) | GET | Retrieves highlight line metadata from an LLMWhisperer extraction job. |
| [Retrieve Extracted Text](actions/retrieve-extracted-text.md) | GET | Retrieves extracted text from an LLMWhisperer extraction job. |
| [Start Extraction From URL](actions/start-extraction.md) | POST | Starts a document extraction job in LLMWhisperer from a URL. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Delete Webhook Endpoint](actions/delete-webhook-endpoint.md) | DELETE | Deletes an existing webhook endpoint from LLMWhisperer. |
| [Get Webhook Details](actions/get-webhook-details.md) | GET | Retrieves a webhook endpoint from LLMWhisperer by name. |
| [Register Webhook Endpoint](actions/register-webhook-endpoint.md) | POST | Registers a webhook endpoint in LLMWhisperer. |
| [Update Webhook Endpoint](actions/update-webhook-endpoint.md) | PUT | Updates an existing webhook endpoint in LLMWhisperer. |

