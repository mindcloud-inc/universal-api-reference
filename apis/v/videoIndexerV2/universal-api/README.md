# <img src="https://images.mindcloud.co/apps/icons/video-indexer_1777994090564.png" alt="Video Indexer (V2) logo" width="28" height="28"> Video Indexer (V2): Universal API

Upload, index, search, and retrieve video insights

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/videoIndexerV2/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://vi.microsoft.com
- **Vendor API docs:** https://learn.microsoft.com/en-us/connectors/videoindexer-v2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Accounts](actions/get-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/get-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Access Token](actions/get-account-access-token.md) | GET | Retrieves an account access token from Video Indexer (V2). |

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from Video Indexer (V2). |
| [Get Accounts](actions/get-accounts.md) | GET | Retrieves accounts from Video Indexer (V2). |

### Face

| Action | Method | Description |
| --- | --- | --- |
| [Update Face Name](actions/update-face-name.md) | PUT | Updates a face name in Video Indexer (V2). |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Delete Video](actions/delete-video.md) | DELETE | Deletes a video from Video Indexer (V2). |
| [List Videos](actions/list-videos.md) | GET | Retrieves videos from Video Indexer (V2). |
| [Re-Index Video](actions/re-index-video.md) | PUT | Re-indexes a video in Video Indexer (V2). |
| [Search Videos](actions/search-videos.md) | GET | Finds videos in Video Indexer (V2) by query. |
| [Upload Video And Index](actions/upload-video-and-index.md) | POST | Uploads and indexes a video in Video Indexer (V2). |

### Video Captions

| Action | Method | Description |
| --- | --- | --- |
| [Get Video Captions](actions/get-video-captions.md) | GET | Retrieves video captions from Video Indexer (V2). |

### Video Id

| Action | Method | Description |
| --- | --- | --- |
| [Get Video ID By External ID](actions/get-video-id-by-external-id.md) | GET | Retrieves a video ID from an external ID in Video Indexer (V2). |

### Video Index

| Action | Method | Description |
| --- | --- | --- |
| [Get Video Index](actions/get-video-index.md) | GET | Retrieves a video's index from Video Indexer (V2). |

### Video Source File

| Action | Method | Description |
| --- | --- | --- |
| [Delete Video Source File](actions/delete-video-source-file.md) | DELETE | Deletes a video's source file from Video Indexer (V2). |

### Video Thumbnail

| Action | Method | Description |
| --- | --- | --- |
| [Get Video Thumbnail](actions/get-video-thumbnail.md) | GET | Retrieves a video thumbnail from Video Indexer (V2). |

### Video Transcript

| Action | Method | Description |
| --- | --- | --- |
| [Update Video Transcript](actions/update-video-transcript.md) | PUT | Updates a video's transcript in Video Indexer (V2). |

