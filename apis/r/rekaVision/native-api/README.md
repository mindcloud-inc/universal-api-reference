# Reka Vision: Native API Reference

A consolidated summary of Reka Vision's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.reka.ai/vision/overview
- **OpenAPI specification:** https://docs.reka.ai/openapi.json?api=5146f567-65cc-4979-aa33-5ba2c1668e3a
- **API base URL:** `https://vision-agent.api.reka.ai`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://docs.reka.ai/resources/faqs)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Chat (V1)](actions/chat-v1.md) | `POST /v1/qa/chat` | [docs](https://docs.reka.ai/vision/api-reference/v-1/chat-v-1-qa-chat-post) |
| [Create Reel (V1)](actions/create-reel-v1.md) | `POST /v1/clips` | [docs](https://docs.reka.ai/vision/api-reference/v-1/create-reel-v-1-clips-post) |
| [Create Video Group (V2)](actions/create-video-group-v2.md) | `POST /v2/video-groups` | [docs](https://docs.reka.ai/vision/api-reference/v-2/create-video-group-v-2-video-groups-post) |
| [Delete Image By Id (V1)](actions/delete-image-by-id-v1.md) | `DELETE /v1/images/:imageId` | [docs](https://docs.reka.ai/vision/api-reference/v-1/delete-image) |
| [Delete Reel (V1)](actions/delete-reel-v1.md) | `DELETE /v1/clips/:id` | [docs](https://docs.reka.ai/vision/api-reference/v-1/delete-reel-v-1-clips-id-delete) |
| [Delete Video By Id (V1)](actions/delete-video-by-id-v1.md) | `DELETE /v1/videos/:videoId` | [docs](https://docs.reka.ai/vision/api-reference/v-1/delete-video) |
| [Delete Video Group (V2)](actions/delete-video-group-v2.md) | `DELETE /v2/video-groups/:groupId` | [docs](https://docs.reka.ai/vision/api-reference/v-2/delete-video-group-v-2-video-groups-group-id-delete) |
| [Delete Video (V2)](actions/delete-video-v2.md) | `DELETE /v2/videos/:videoId` | [docs](https://docs.reka.ai/vision/api-reference/v-2/delete-video-v-2-videos-video-id-delete) |
| [Embedding Search (V1)](actions/embedding-search-v1.md) | `POST /v1/videos/search` | [docs](https://docs.reka.ai/vision/api-reference/v-1/post-embedding-search) |
| [Get Feature Catalog (V2)](actions/get-feature-catalog-v2.md) | `GET /v2/features` | [docs](https://docs.reka.ai/vision/api-reference/v-2/get-feature-catalog-v-2-features-get) |
| [Get Image By Id (V1)](actions/get-image-by-id-v1.md) | `GET /v1/images/:imageId` | [docs](https://docs.reka.ai/vision/api-reference/v-1/get-image) |
| [Get Reel (V1)](actions/get-reel-v1.md) | `GET /v1/clips/:id` | [docs](https://docs.reka.ai/vision/api-reference/v-1/get-reel-v-1-clips-id-get) |
| [Get Video By Id (V1)](actions/get-video-by-id-v1.md) | `GET /v1/videos/:videoId` | [docs](https://docs.reka.ai/vision/api-reference/v-1/get-video) |
| [Get Video Group (V2)](actions/get-video-group-v2.md) | `GET /v2/video-groups/:groupId` | [docs](https://docs.reka.ai/vision/api-reference/v-2/get-video-group-v-2-video-groups-group-id-get) |
| [Get Video (V2)](actions/get-video-v2.md) | `GET /v2/videos/:videoId` | [docs](https://docs.reka.ai/vision/api-reference/v-2/get-video-v-2-videos-video-id-get) |
| [Health Check](actions/health-check.md) | `GET /health` | [docs](https://docs.reka.ai/vision/overview) |
| [Indexed Tag (V1)](actions/indexed-tag-v1.md) | `POST /v1/qa/indexedtag` | [docs](https://docs.reka.ai/vision/api-reference/v-1/indexed-tag-v-1-qa-indexedtag-post) |
| [List Captions (V2)](actions/list-captions-v2.md) | `GET /v2/videos/:videoId/captions` | [docs](https://docs.reka.ai/vision/api-reference/v-2/list-captions-v-2-videos-video-id-captions-get) |
| [List Group Videos (V2)](actions/list-group-videos-v2.md) | `GET /v2/video-groups/:groupId/videos` | [docs](https://docs.reka.ai/vision/api-reference/v-2/list-group-videos-v-2-video-groups-group-id-videos-get) |
| [List Images (V1)](actions/list-images-v1.md) | `GET /v1/images` | [docs](https://docs.reka.ai/vision/api-reference/v-1/get-images) |
| [List Objects (V2)](actions/list-objects-v2.md) | `GET /v2/videos/:videoId/objects` | [docs](https://docs.reka.ai/vision/api-reference/v-2/list-objects-v-2-videos-video-id-objects-get) |
| [List Reels (V1)](actions/list-reels-v1.md) | `GET /v1/clips` | [docs](https://docs.reka.ai/vision/api-reference/v-1/list-reels-v-1-clips-get) |
| [List Scenes (V2)](actions/list-scenes-v2.md) | `GET /v2/videos/:videoId/scenes` | [docs](https://docs.reka.ai/vision/api-reference/v-2/list-scenes-v-2-videos-video-id-scenes-get) |
| [List Transcript (V2)](actions/list-transcript-v2.md) | `GET /v2/videos/:videoId/transcript` | [docs](https://docs.reka.ai/vision/api-reference/v-2/list-transcript-v-2-videos-video-id-transcript-get) |
| [List Video Groups (V2)](actions/list-video-groups-v2.md) | `GET /v2/video-groups` | [docs](https://docs.reka.ai/vision/api-reference/v-2/list-video-groups-v-2-video-groups-get) |
| [List Videos (V1)](actions/list-videos-v1.md) | `GET /v1/videos` | [docs](https://docs.reka.ai/vision/api-reference/v-1/get-videos) |
| [List Videos (V2)](actions/list-videos-v2.md) | `GET /v2/videos` | [docs](https://docs.reka.ai/vision/api-reference/v-2/list-videos-v-2-videos-get) |
| [Move Videos To Group (V2)](actions/move-videos-to-group-v2.md) | `POST /v2/video-groups/:groupId/videos` | [docs](https://docs.reka.ai/vision/api-reference/v-2/move-videos-to-group-v-2-video-groups-group-id-videos-post) |
| [Plan Features (V2)](actions/plan-features-v2.md) | `POST /v2/videos/:videoId/features/plan` | [docs](https://docs.reka.ai/vision/api-reference/v-2/plan-features-v-2-videos-video-id-features-plan-post) |
| [Quick Tag (V1)](actions/quick-tag-v1.md) | `POST /v1/qa/quicktag` | [docs](https://docs.reka.ai/vision/api-reference/v-1/quick-tag-v-1-qa-quicktag-post) |
| [Search Images (V1)](actions/search-images-v1.md) | `POST /v1/images/search` | [docs](https://docs.reka.ai/vision/api-reference/v-1/search-images-v-1-images-search-post) |
| [Trigger Captions (V2)](actions/trigger-captions-v2.md) | `POST /v2/videos/:videoId/features/captions` | [docs](https://docs.reka.ai/vision/api-reference/v-2/trigger-captions-v-2-videos-video-id-features-captions-post) |
| [Trigger Embeddings (V2)](actions/trigger-embeddings-v2.md) | `POST /v2/videos/:videoId/features/embeddings` | [docs](https://docs.reka.ai/vision/api-reference/v-2/trigger-embeddings-v-2-videos-video-id-features-embeddings-post) |
| [Trigger Objects (V2)](actions/trigger-objects-v2.md) | `POST /v2/videos/:videoId/features/objects` | [docs](https://docs.reka.ai/vision/api-reference/v-2/trigger-objects-v-2-videos-video-id-features-objects-post) |
| [Trigger Transcript (V2)](actions/trigger-transcript-v2.md) | `POST /v2/videos/:videoId/features/transcript` | [docs](https://docs.reka.ai/vision/api-reference/v-2/trigger-transcript-v-2-videos-video-id-features-transcript-post) |
| [Update Video Group (V2)](actions/update-video-group-v2.md) | `PATCH /v2/video-groups/:groupId` | [docs](https://docs.reka.ai/vision/api-reference/v-2/update-video-group-v-2-video-groups-group-id-patch) |
| [Update Video Metadata (V2)](actions/update-video-metadata-v2.md) | `PATCH /v2/videos/:videoId` | [docs](https://docs.reka.ai/vision/api-reference/v-2/update-video-metadata-v-2-videos-video-id-patch) |
| [Upload Images (V1)](actions/upload-images-v1.md) | `POST /v1/images/upload` | [docs](https://docs.reka.ai/vision/api-reference/v-1/upload-images-v-1-images-upload-post) |
| [Upload Video (V1)](actions/upload-video-v1.md) | `POST /v1/videos/upload` | [docs](https://docs.reka.ai/vision/api-reference/v-1/upload) |
| [Upload Video (V2)](actions/upload-video-v2.md) | `POST /v2/videos` | [docs](https://docs.reka.ai/vision/api-reference/v-2/upload-video-v-2-videos-post) |
