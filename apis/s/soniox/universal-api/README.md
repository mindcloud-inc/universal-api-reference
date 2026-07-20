# <img src="https://images.mindcloud.co/apps/icons/soniox-icon_1775768069191.png" alt="Soniox logo" width="28" height="28"> Soniox: Universal API

Transcribe audio, manage files, and retrieve transcripts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/soniox/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://soniox.com
- **Vendor API docs:** https://soniox.com/docs/stt/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get models](actions/get-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/soniox/latest/actions/get-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Delete file](actions/delete-file.md) | DELETE | Deletes an existing file from Soniox. |
| [Get file](actions/get-file.md) | GET | Retrieves a file from Soniox. |
| [Get files](actions/get-files.md) | GET | Retrieves uploaded files from Soniox. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Create transcription](actions/create-transcription.md) | POST | Creates a new transcription in Soniox. |
| [Delete transcription](actions/delete-transcription.md) | DELETE | Deletes an existing transcription from Soniox. |
| [Get transcription](actions/get-transcription.md) | GET | Retrieves a transcription from Soniox. |
| [Get transcription transcript](actions/get-transcription-transcript.md) | GET | Retrieves transcript text for a Soniox transcription. |
| [Get transcriptions](actions/get-transcriptions.md) | GET | Retrieves transcriptions from Soniox. |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [Get models](actions/get-models.md) | GET | Retrieves available transcription models from Soniox. |

