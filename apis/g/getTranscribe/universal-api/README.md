# <img src="https://images.mindcloud.co/apps/icons/gettranscribe-icon_1775827732256.png" alt="GetTranscribe logo" width="28" height="28"> GetTranscribe: Universal API

GetTranscribe API wrapper for managing video transcriptions, folders, and user account data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/getTranscribe/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.gettranscribe.ai
- **Vendor API docs:** https://www.gettranscribe.ai/api-documentation/authentication

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Folders](actions/list-folders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getTranscribe/latest/actions/list-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a folder in GetTranscribe. |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from GetTranscribe. |
| [Update Folder](actions/update-folder.md) | PUT | Updates a folder in GetTranscribe. |

### Transcription

| Action | Method | Description |
| --- | --- | --- |
| [Create Transcription](actions/create-transcription.md) | POST | Creates a transcription in GetTranscribe from a video URL. |
| [Get Transcription](actions/get-transcription.md) | GET | Retrieves a transcription from GetTranscribe by ID. |
| [List Transcriptions](actions/list-transcriptions.md) | GET | Retrieves transcriptions from GetTranscribe by filters. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | GET | Retrieves user account details from GetTranscribe. |

