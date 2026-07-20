# <img src="https://images.mindcloud.co/apps/icons/favicon-www-temi-com-48x48_1777047281053.png" alt="Temi logo" width="28" height="28"> Temi: Universal API

Transcribe audio and video with Temi, list transcription jobs, retrieve transcripts, share editor links, and manage account details.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/temi/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.temi.com/api
- **Vendor API docs:** https://www.temi.com/api/reference/v1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Details](actions/get-account-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/temi/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Details](actions/get-account-details.md) | GET | Retrieves Temi account details. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST | Creates a transcription job in Temi. |
| [Delete Job](actions/delete-job.md) | DELETE | Deletes a transcription job from Temi. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves transcription jobs from Temi. |

### Transcript Share Link

| Action | Method | Description |
| --- | --- | --- |
| [Share Transcript Editor URL](actions/share-transcript-editor-url.md) | POST | Creates a shareable transcript editor URL in Temi. |

