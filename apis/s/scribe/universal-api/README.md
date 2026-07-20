# <img src="https://images.mindcloud.co/apps/icons/scribe_1774978435362.png" alt="3Scribe logo" width="28" height="28"> 3Scribe: Universal API

3Scribe transcribes media files and manages transcription jobs through the 3Scribe Developer API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scribe/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://3scri.be
- **Vendor API docs:** https://helpcentre.3scri.be/developers/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Transcription Jobs](actions/list-transcription-jobs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scribe/latest/actions/list-transcription-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Transcription Job Via Pre-Signed URL](actions/create-transcription-job-via-pre-signed-url.md) | POST | Creates a new transcription job in 3Scribe from a pre-signed upload URL. |
| [Create Transcription Job Via Public URL](actions/create-transcription-job-via-public-url.md) | POST | Creates a new transcription job in 3Scribe from a public URL. |
| [Delete Transcription Job](actions/delete-transcription-job.md) | DELETE | Deletes an existing transcription job from 3Scribe. |
| [Get Transcription Job](actions/get-transcription-job.md) | GET | Retrieves a transcription job from 3Scribe. |
| [List Transcription Jobs](actions/list-transcription-jobs.md) | GET | Retrieves transcription jobs from your 3Scribe account. |

