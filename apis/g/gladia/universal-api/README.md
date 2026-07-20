# <img src="https://images.mindcloud.co/apps/icons/66d1739eb3d771283bb9e675-favicon_1774534973997.png" alt="Gladia logo" width="28" height="28"> Gladia: Universal API

Gladia: Transcribe audio, stream speech, and extract voice insights

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gladia/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.gladia.io
- **Vendor API docs:** https://docs.gladia.io/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Pre-recorded Transcriptions](actions/list-pre-recorded-transcriptions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gladia/latest/actions/list-pre-recorded-transcriptions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Audio File

| Action | Method | Description |
| --- | --- | --- |
| [Upload Audio File](actions/upload-audio-file.md) | POST | Uploads an audio file to Gladia. |

### Job History Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Job History](actions/list-job-history.md) | GET | Retrieves historical job records from Gladia. |

### Legacy Audio Transcription

| Action | Method | Description |
| --- | --- | --- |
| [Create Legacy Audio Transcription](actions/create-legacy-audio-transcription.md) | POST | Creates a legacy audio transcription job in Gladia. |

### Legacy Video Transcription

| Action | Method | Description |
| --- | --- | --- |
| [Create Legacy Video Transcription](actions/create-legacy-video-transcription.md) | POST | Creates a legacy video transcription job in Gladia. |

### Live Audio File

| Action | Method | Description |
| --- | --- | --- |
| [Download Live Audio File](actions/download-live-audio-file.md) | GET | Retrieves a live transcription recording from Gladia. |

### Live Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Live Job](actions/create-live-job.md) | POST | Creates a live transcription job in Gladia. |
| [Delete Live Job](actions/delete-live-job.md) | DELETE | Deletes a live job from Gladia. |
| [Get Live Job](actions/get-live-job.md) | GET | Retrieves a live job's status, parameters, and result from Gladia. |
| [List Live Jobs](actions/list-live-jobs.md) | GET | Retrieves live jobs from Gladia. |
| [Update Live Job Debug Params](actions/update-live-job-debug-params.md) | PUT | Updates live job debug parameters in Gladia. |

### Pre-recorded Audio File

| Action | Method | Description |
| --- | --- | --- |
| [Download Pre-recorded Audio File](actions/download-pre-recorded-audio-file.md) | GET | Retrieves a pre-recorded audio file from Gladia. |

### Pre-recorded Transcription

| Action | Method | Description |
| --- | --- | --- |
| [Create Pre-recorded Transcription](actions/create-pre-recorded-transcription.md) | POST | Creates a pre-recorded transcription job in Gladia. |
| [Delete Pre-recorded Transcription](actions/delete-pre-recorded-transcription.md) | DELETE | Deletes a pre-recorded transcription job from Gladia. |
| [Get Pre-recorded Transcription](actions/get-pre-recorded-transcription.md) | GET | Retrieves a pre-recorded job's status, parameters, and result from Gladia. |
| [List Pre-recorded Transcriptions](actions/list-pre-recorded-transcriptions.md) | GET | Retrieves pre-recorded transcription jobs from Gladia. |

### Transcription

| Action | Method | Description |
| --- | --- | --- |
| [Create Transcription](actions/create-transcription.md) | POST | Creates a transcription job in Gladia. |
| [Delete Transcription](actions/delete-transcription.md) | DELETE | Deletes a transcription job from Gladia. |
| [Get Transcription](actions/get-transcription.md) | GET | Retrieves a transcription job's status, parameters, and result from Gladia. |
| [List Transcriptions](actions/list-transcriptions.md) | GET | Retrieves transcription jobs from the Gladia API. |

### Transcription Audio File

| Action | Method | Description |
| --- | --- | --- |
| [Download Transcription Audio File](actions/download-transcription-audio-file.md) | GET | Retrieves a transcription audio file from Gladia. |

