# <img src="https://images.mindcloud.co/apps/icons/screenshot-2026-05-06-at-14_1778088981091.png" alt="Speech is Cheap logo" width="28" height="28"> Speech is Cheap: Universal API

Speech is Cheap provides low-cost speech-to-text transcription jobs for publicly accessible audio and video files, with optional speaker, word, language, privacy, and webhook controls.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/speechIsCheap/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://speechischeap.com/
- **Vendor API docs:** https://docs.speechischeap.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API Health](actions/get-api-health.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/speechIsCheap/latest/actions/get-api-health?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Api Health

| Action | Method | Description |
| --- | --- | --- |
| [Get API Health](actions/get-api-health.md) | GET | Retrieves Speech is Cheap API health status. |

### Transcription Job

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Transcription Job](actions/cancel-transcription-job.md) | DELETE | Deletes a pending transcription job from Speech is Cheap. |
| [Create Transcription Job](actions/create-transcription-job.md) | POST | Creates a new transcription job in Speech is Cheap. |
| [Get Transcription Job](actions/get-transcription-job.md) | GET | Retrieves a transcription job from Speech is Cheap. |

