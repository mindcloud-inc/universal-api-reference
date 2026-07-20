# <img src="https://images.mindcloud.co/apps/icons/mindee_1774273276873.png" alt="Mindee logo" width="28" height="28"> Mindee: Universal API

Extract document data, classify files, crop pages, and run OCR

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mindee/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mindee.com
- **Vendor API docs:** https://docs.mindee.com/integrations/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Job Status](actions/get-job-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindee/latest/actions/get-job-status?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Status](actions/get-job-status.md) | GET | Retrieves a job status from Mindee. |
| [Start Classification Job From URL](actions/start-classification-job-from-url.md) | POST | Creates a new classification job in Mindee from a URL. |
| [Start Crop Job From URL](actions/start-crop-job-from-url.md) | POST | Creates a new crop job in Mindee from a URL. |
| [Start Extraction Job From URL](actions/start-extraction-job-from-url.md) | POST | Creates a new extraction job in Mindee from a URL. |
| [Start OCR Job From URL](actions/start-ocr-job-from-url.md) | POST | Creates a new OCR job in Mindee from a URL. |
| [Start Split Job From URL](actions/start-split-job-from-url.md) | POST | Creates a new split job in Mindee from a URL. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Classification Result](actions/get-classification-result.md) | GET | Retrieves a classification result from Mindee. |
| [Get Crop Result](actions/get-crop-result.md) | GET | Retrieves a crop result from Mindee. |
| [Get Extraction Result](actions/get-extraction-result.md) | GET | Retrieves an extraction result from Mindee. |
| [Get OCR Result](actions/get-ocr-result.md) | GET | Retrieves an OCR result from Mindee. |
| [Get Split Result](actions/get-split-result.md) | GET | Retrieves a split result from Mindee. |

