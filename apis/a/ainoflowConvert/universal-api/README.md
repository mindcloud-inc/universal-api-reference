# <img src="https://images.mindcloud.co/apps/icons/ainoflow-convert_1775768300753.png" alt="Ainoflow Convert logo" width="28" height="28"> Ainoflow Convert: Universal API

Ainoflow Convert API wrapper for document processing, OCR, and audio transcription.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ainoflowConvert/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ainoflow.io/
- **Vendor API docs:** https://www.ainoflow.io/docs/api/convert

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Job Status](actions/get-job-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ainoflowConvert/latest/actions/get-job-status?connectionId=$CONNECTION_ID&jobId=00000000-0000-0000-0000-000000000000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Conversion Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Status](actions/get-job-status.md) | GET | Retrieves conversion job status and download URLs from Ainoflow Convert. |

### Conversion Submission

| Action | Method | Description |
| --- | --- | --- |
| [Submit Base64 Document](actions/submit-base64-document.md) | POST | Creates a conversion job in Ainoflow Convert from base64 content. |
| [Submit External URL](actions/submit-external-url.md) | POST | Creates a conversion job in Ainoflow Convert from an external URL. |
| [Submit File for Processing](actions/submit-file-for-processing.md) | POST | Creates a conversion job in Ainoflow Convert from an uploaded file. |

