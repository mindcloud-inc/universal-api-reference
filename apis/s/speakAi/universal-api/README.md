# <img src="https://images.mindcloud.co/apps/icons/speak-ai_1773958307887.png" alt="Speak Ai logo" width="28" height="28"> Speak Ai: Universal API

Upload audio, video, or text to Speak Ai, retrieve transcripts and insights, manage folders and recorders, and export analyzed content.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/speakAi/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://speakai.co/
- **Vendor API docs:** https://docs.speakai.co/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Request Access Token](actions/request-access-token.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/request-access-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Export Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Export Content](actions/export-content.md) | POST | Creates a content export in Speak Ai. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Delete Media](actions/delete-media.md) | DELETE | Deletes an existing media item from Speak Ai. |
| [Get Media Insight](actions/get-media-insight.md) | GET | Retrieves media insights from Speak Ai. |
| [Get Media Status](actions/get-media-status.md) | GET | Retrieves media status details from Speak Ai. |
| [Get Media Transcript](actions/get-media-transcript.md) | GET | Retrieves a media transcript from Speak Ai. |
| [Get Upload Signed URL](actions/get-upload-signed-url.md) | GET | Retrieves an upload signed URL from Speak Ai. |
| [List Media](actions/list-media.md) | GET | Retrieves media from Speak Ai. |
| [Update Media](actions/update-media.md) | PUT | Updates an existing media item in Speak Ai. |
| [Update Media Speakers](actions/update-media-speakers.md) | PUT | Updates transcript speaker names in Speak Ai. |
| [Upload Media](actions/upload-media.md) | POST | Creates a media file in Speak Ai. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a folder in Speak Ai. |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes an existing folder from Speak Ai. |
| [Get Folder](actions/get-folder.md) | GET | Retrieves folder details from Speak Ai. |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from Speak Ai. |
| [Update Folder](actions/update-folder.md) | PUT | Updates an existing folder in Speak Ai. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Text Note](actions/create-text-note.md) | POST | Creates a text note in Speak Ai. |
| [Delete Text Note](actions/delete-text-note.md) | DELETE | Deletes an existing text note from Speak Ai. |
| [Get Text Insight](actions/get-text-insight.md) | GET | Retrieves text insights from Speak Ai. |
| [Reanalyze Text](actions/reanalyze-text.md) | PUT |  |
| [Update Text Note](actions/update-text-note.md) | PUT | Updates an existing text note in Speak Ai. |

### Recordings

| Action | Method | Description |
| --- | --- | --- |
| [Create Recorder](actions/create-recorder.md) | POST | Creates a recorder in Speak Ai. |
| [Get Recorder](actions/get-recorder.md) | GET | Retrieves recorder details from Speak Ai. |
| [List Recorders](actions/list-recorders.md) | GET | Retrieves recorders from Speak Ai. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Request Access Token](actions/request-access-token.md) | GET | Requests an access token from Speak Ai. |

