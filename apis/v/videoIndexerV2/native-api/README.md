# Video Indexer (V2): Native API Reference

A consolidated summary of Video Indexer (V2)'s API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/connectors/videoindexer-v2/
- **API base URL:** `https://api.videoindexer.ai`

## Authentication

### API Key

Authenticate requests with an Azure AI Video Indexer API Management subscription key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Ocp-Apim-Subscription-Key: <apiKey>
```

[Official authentication documentation](https://learn.microsoft.com/en-us/azure/azure-video-indexer/video-indexer-use-apis)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size. Use `skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Video](actions/delete-video.md) | `DELETE /:location/Accounts/:accountId/Videos/:videoId` | [docs](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#delete-video) |
| [Delete Video Source File](actions/delete-video-source-file.md) | `DELETE /:location/Accounts/:accountId/Videos/:videoId/SourceFile` | [docs](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#delete-video-source-file) |
| [Get Account](actions/get-account.md) | `GET /:location/Accounts/:accountId` | [docs](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#get-account) |
| [Get Account Access Token](actions/get-account-access-token.md) | `GET /Auth/:location/Accounts/:accountId/AccessToken` | [docs](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#get-account-access-token) |
| [Get Accounts](actions/get-accounts.md) | `GET /Auth/trial/Accounts` | [docs](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#get-accounts) |
| [Get Video Captions](actions/get-video-captions.md) | `GET /:location/Accounts/:accountId/Videos/:videoId/Captions` | [docs](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#get-video-captions) |
| [Get Video ID By External ID](actions/get-video-id-by-external-id.md) | `GET /:location/Accounts/:accountId/Videos/GetIdByExternalId` | [docs](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#get-video-id-by-external-id) |
| [Get Video Index](actions/get-video-index.md) | `GET /:location/Accounts/:accountId/Videos/:videoId/Index` | [docs](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#get-video-index) |
| [Get Video Thumbnail](actions/get-video-thumbnail.md) | `GET /:location/Accounts/:accountId/Videos/:videoId/Thumbnails/:thumbnailId` | [docs](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#get-video-thumbnail) |
| [List Videos](actions/list-videos.md) | `GET /:location/Accounts/:accountId/Videos` | [docs](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#list-videos) |
| [Re-Index Video](actions/re-index-video.md) | `PUT /:location/Accounts/:accountId/Videos/:videoId/Index` | [docs](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#re-index-video) |
| [Search Videos](actions/search-videos.md) | `GET /:location/Accounts/:accountId/Videos/Search` | [docs](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#search-videos) |
| [Update Face Name](actions/update-face-name.md) | `PUT /:location/Accounts/:accountId/Videos/:videoId/Index/Faces/:faceId` | [docs](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#update-face-name) |
| [Update Video Transcript](actions/update-video-transcript.md) | `PUT /:location/Accounts/:accountId/Videos/:videoId/Index/Transcript` | [docs](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#update-video-transcript) |
| [Upload Video And Index](actions/upload-video-and-index.md) | `POST /:location/Accounts/:accountId/Videos` | [docs](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#upload-video-and-index) |
