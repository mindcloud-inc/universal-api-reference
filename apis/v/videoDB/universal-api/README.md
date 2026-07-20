# <img src="https://images.mindcloud.co/apps/icons/video-db_1774470863013.png" alt="VideoDB logo" width="28" height="28"> VideoDB: Universal API

Upload, search, and analyze video, audio, and image content

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/videoDB/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://videodb.io
- **Vendor API docs:** https://docs.videodb.io/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Videos](actions/list-videos.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/videoDB/latest/actions/list-videos?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST | Creates a new collection in VideoDB. |
| [Delete Collection](actions/delete-collection.md) | DELETE | Deletes an existing collection from VideoDB. |
| [Get Collection](actions/get-collection.md) | GET | Retrieves a collection from VideoDB. |
| [List Collections](actions/list-collections.md) | GET | Retrieves collections from VideoDB. |
| [Update Collection](actions/update-collection.md) | PUT | Updates an existing collection in VideoDB. |

### Transcription

| Action | Method | Description |
| --- | --- | --- |
| [Get Video Transcription](actions/get-video-transcription.md) | GET | Retrieves a video transcription from VideoDB. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Delete Video](actions/delete-video.md) | DELETE | Deletes an existing video from VideoDB. |
| [Get Video Details](actions/get-video-details.md) | GET | Retrieves video details from VideoDB. |
| [List Videos](actions/list-videos.md) | GET | Retrieves videos from VideoDB. |
| [Update Video](actions/update-video.md) | PUT | Updates an existing video in VideoDB. |
| [Upload to Collection](actions/upload-to-collection.md) | POST | Uploads media to a collection in VideoDB. |

