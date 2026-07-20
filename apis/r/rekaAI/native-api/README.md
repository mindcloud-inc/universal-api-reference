# Reka AI: Native API Reference

A consolidated summary of Reka AI's API configuration and 50 documented operations, with links to official documentation.

- **Official docs:** https://docs.reka.ai/overview
- **API base URL:** `https://api.reka.ai`

## Authentication

### API Key

Use a Reka API key for bearer-authenticated API access.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.reka.ai/getting-started/quickstart)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (50 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Ask Video QA](actions/ask-video-qa.md) | `POST https://vision-agent.api.reka.ai/v1/qa/chat` | [docs](https://docs.reka.ai/vision/api-reference/video-qa/chat-v-1-qa-chat-post) |
| [Create Chat Completion](actions/create-chat-completion.md) | `POST /v1/chat/completions` | [docs](https://docs.reka.ai/chat/api-reference/create) |
| [Create Legacy Video Group](actions/create-legacy-video-group.md) | `POST https://vision-agent.api.reka.ai/v1/video-groups` | [docs](https://docs.reka.ai/vision/api-reference/video-groups/post-create-video-group) |
| [Create Reel](actions/create-reel.md) | `POST https://vision-agent.api.reka.ai/v1/clips` | [docs](https://docs.reka.ai/vision/api-reference/clip-generation/create-reel-v-1-clips-post) |
| [Create Research Chat Completion](actions/create-research-chat-completion.md) | `POST /v1/chat/completions` | [docs](https://docs.reka.ai/research/api-reference/create-chat-completion) |
| [Create Video Group](actions/create-video-group.md) | `POST https://vision-agent.api.reka.ai/v2/video-groups` | [docs](https://docs.reka.ai/vision/api-reference/v-2/create-video-group-v-2-video-groups-post) |
| [Delete Image](actions/delete-image.md) | `DELETE https://vision-agent.api.reka.ai/v1/images/:image_id` | [docs](https://docs.reka.ai/vision/api-reference/image-management/delete-image) |
| [Delete Legacy Video](actions/delete-legacy-video.md) | `DELETE https://vision-agent.api.reka.ai/v1/videos/:video_id` | [docs](https://docs.reka.ai/vision/api-reference/video-management/delete-video) |
| [Delete Legacy Video Group](actions/delete-legacy-video-group.md) | `DELETE https://vision-agent.api.reka.ai/v1/video-groups/:group_id` | [docs](https://docs.reka.ai/vision/api-reference/video-groups/delete-video-group) |
| [Delete Reel](actions/delete-reel.md) | `DELETE https://vision-agent.api.reka.ai/v1/clips/:id` | [docs](https://docs.reka.ai/vision/api-reference/clip-generation/delete-reel-v-1-clips-id-delete) |
| [Delete Video](actions/delete-video.md) | `DELETE https://vision-agent.api.reka.ai/v2/videos/:video_id` | [docs](https://docs.reka.ai/vision/api-reference/v-2/delete-video-v-2-videos-video-id-delete) |
| [Delete Video Group](actions/delete-video-group.md) | `DELETE https://vision-agent.api.reka.ai/v2/video-groups/:group_id` | [docs](https://docs.reka.ai/vision/api-reference/v-2/delete-video-group-v-2-video-groups-group-id-delete) |
| [Get Feature Catalog](actions/get-feature-catalog.md) | `GET https://vision-agent.api.reka.ai/v2/features` | [docs](https://docs.reka.ai/vision/api-reference/v-2/get-feature-catalog-v-2-features-get) |
| [Get Image](actions/get-image.md) | `GET https://vision-agent.api.reka.ai/v1/images/:image_id` | [docs](https://docs.reka.ai/vision/api-reference/image-management/get-image) |
| [Get Images](actions/get-images.md) | `GET https://vision-agent.api.reka.ai/v1/images` | [docs](https://docs.reka.ai/vision/api-reference/image-management/get-images) |
| [Get Legacy Video](actions/get-legacy-video.md) | `GET https://vision-agent.api.reka.ai/v1/videos/:video_id` | [docs](https://docs.reka.ai/vision/api-reference/video-management/get-video) |
| [Get Legacy Video Group](actions/get-legacy-video-group.md) | `GET https://vision-agent.api.reka.ai/v1/video-groups/:group_id` | [docs](https://docs.reka.ai/vision/api-reference/video-groups/get-video-group) |
| [Get Reel](actions/get-reel.md) | `GET https://vision-agent.api.reka.ai/v1/clips/:id` | [docs](https://docs.reka.ai/vision/api-reference/clip-generation/get-reel-v-1-clips-id-get) |
| [Get Video](actions/get-video.md) | `GET https://vision-agent.api.reka.ai/v2/videos/:video_id` | [docs](https://docs.reka.ai/vision/api-reference/v-2/get-video-v-2-videos-video-id-get) |
| [Get Video Group](actions/get-video-group.md) | `GET https://vision-agent.api.reka.ai/v2/video-groups/:group_id` | [docs](https://docs.reka.ai/vision/api-reference/v-2/get-video-group-v-2-video-groups-group-id-get) |
| [Indexed Tag Video](actions/indexed-tag-video.md) | `POST https://vision-agent.api.reka.ai/v1/qa/indexedtag` | [docs](https://docs.reka.ai/vision/api-reference/metadata-tagging/indexed-tag-v-1-qa-indexedtag-post) |
| [List Captions](actions/list-captions.md) | `GET https://vision-agent.api.reka.ai/v2/videos/:video_id/captions` | [docs](https://docs.reka.ai/vision/api-reference/v-2/list-captions-v-2-videos-video-id-captions-get) |
| [List Group Videos](actions/list-group-videos.md) | `GET https://vision-agent.api.reka.ai/v2/video-groups/:group_id/videos` | [docs](https://docs.reka.ai/vision/api-reference/v-2/list-group-videos-v-2-video-groups-group-id-videos-get) |
| [List Legacy Group Videos](actions/list-legacy-group-videos.md) | `GET https://vision-agent.api.reka.ai/v1/videos/groups/:group_id/videos` | [docs](https://docs.reka.ai/vision/api-reference/video-groups/list-group-videos-v-1-videos-groups-group-id-videos-get) |
| [List Legacy Video Groups](actions/list-legacy-video-groups.md) | `GET https://vision-agent.api.reka.ai/v1/video-groups` | [docs](https://docs.reka.ai/vision/api-reference/video-groups/get-list-video-groups) |
| [List Legacy Videos](actions/list-legacy-videos.md) | `GET https://vision-agent.api.reka.ai/v1/videos` | [docs](https://docs.reka.ai/vision/api-reference/video-management/get-videos) |
| [List Models](actions/list-models.md) | `GET /v1/models` | [docs](https://docs.reka.ai/chat/api-reference/get) |
| [List Objects](actions/list-objects.md) | `GET https://vision-agent.api.reka.ai/v2/videos/:video_id/objects` | [docs](https://docs.reka.ai/vision/api-reference/v-2/list-objects-v-2-videos-video-id-objects-get) |
| [List Reels](actions/list-reels.md) | `GET https://vision-agent.api.reka.ai/v1/clips` | [docs](https://docs.reka.ai/vision/api-reference/clip-api/list-reels-v-1-clips-get) |
| [List Scenes](actions/list-scenes.md) | `GET https://vision-agent.api.reka.ai/v2/videos/:video_id/scenes` | [docs](https://docs.reka.ai/vision/api-reference/v-2/list-scenes-v-2-videos-video-id-scenes-get) |
| [List Transcript](actions/list-transcript.md) | `GET https://vision-agent.api.reka.ai/v2/videos/:video_id/transcript` | [docs](https://docs.reka.ai/vision/api-reference/v-2/list-transcript-v-2-videos-video-id-transcript-get) |
| [List Video Groups](actions/list-video-groups.md) | `GET https://vision-agent.api.reka.ai/v2/video-groups` | [docs](https://docs.reka.ai/vision/api-reference/v-2/list-video-groups-v-2-video-groups-get) |
| [List Videos](actions/list-videos.md) | `GET https://vision-agent.api.reka.ai/v2/videos` | [docs](https://docs.reka.ai/vision/api-reference/v-2/list-videos-v-2-videos-get) |
| [Move Videos To Group](actions/move-videos-to-group.md) | `POST https://vision-agent.api.reka.ai/v2/video-groups/:group_id/videos` | [docs](https://docs.reka.ai/vision/api-reference/v-2/move-videos-to-group-v-2-video-groups-group-id-videos-post) |
| [Move Videos To Legacy Group](actions/move-videos-to-legacy-group.md) | `POST https://vision-agent.api.reka.ai/v1/videos/group` | [docs](https://docs.reka.ai/vision/api-reference/video-group/post-move-videos-to-group) |
| [Plan Features](actions/plan-features.md) | `POST https://vision-agent.api.reka.ai/v2/videos/:video_id/features/plan` | [docs](https://docs.reka.ai/vision/api-reference/v-2/plan-features-v-2-videos-video-id-features-plan-post) |
| [Quick Tag Video](actions/quick-tag-video.md) | `POST https://vision-agent.api.reka.ai/v1/qa/quicktag` | [docs](https://docs.reka.ai/vision/api-reference/metadata-tagging/quick-tag-v-1-qa-quicktag-post) |
| [Search Images](actions/search-images.md) | `POST https://vision-agent.api.reka.ai/v1/images/search` | [docs](https://docs.reka.ai/vision/api-reference/image-search/search-images-v-1-images-search-post) |
| [Search Videos](actions/search-videos.md) | `POST https://vision-agent.api.reka.ai/v1/videos/search` | [docs](https://docs.reka.ai/vision/api-reference/video-search/post-embedding-search) |
| [Transcribe or Translate Audio](actions/transcribe-or-translate-audio.md) | `POST /v1/transcription_or_translation` | [docs](https://docs.reka.ai/speech/api-reference/transcribe-or-translate) |
| [Trigger Captions](actions/trigger-captions.md) | `POST https://vision-agent.api.reka.ai/v2/videos/:video_id/features/captions` | [docs](https://docs.reka.ai/vision/api-reference/v-2/trigger-captions-v-2-videos-video-id-features-captions-post) |
| [Trigger Embeddings](actions/trigger-embeddings.md) | `POST https://vision-agent.api.reka.ai/v2/videos/:video_id/features/embeddings` | [docs](https://docs.reka.ai/vision/api-reference/v-2/trigger-embeddings-v-2-videos-video-id-features-embeddings-post) |
| [Trigger Objects](actions/trigger-objects.md) | `POST https://vision-agent.api.reka.ai/v2/videos/:video_id/features/objects` | [docs](https://docs.reka.ai/vision/api-reference/v-2/trigger-objects-v-2-videos-video-id-features-objects-post) |
| [Trigger Transcript](actions/trigger-transcript.md) | `POST https://vision-agent.api.reka.ai/v2/videos/:video_id/features/transcript` | [docs](https://docs.reka.ai/vision/api-reference/v-2/trigger-transcript-v-2-videos-video-id-features-transcript-post) |
| [Update Legacy Video Group](actions/update-legacy-video-group.md) | `PATCH https://vision-agent.api.reka.ai/v1/video-groups/:group_id` | [docs](https://docs.reka.ai/vision/api-reference/video-groups/patch-update-video-group) |
| [Update Video Group](actions/update-video-group.md) | `PATCH https://vision-agent.api.reka.ai/v2/video-groups/:group_id` | [docs](https://docs.reka.ai/vision/api-reference/v-2/update-video-group-v-2-video-groups-group-id-patch) |
| [Update Video Metadata](actions/update-video-metadata.md) | `PATCH https://vision-agent.api.reka.ai/v2/videos/:video_id` | [docs](https://docs.reka.ai/vision/api-reference/v-2/update-video-metadata-v-2-videos-video-id-patch) |
| [Upload Images](actions/upload-images.md) | `POST https://vision-agent.api.reka.ai/v1/images/upload` | [docs](https://docs.reka.ai/vision/api-reference/image-management/upload-images-v-1-images-upload-post) |
| [Upload Legacy Video](actions/upload-legacy-video.md) | `POST https://vision-agent.api.reka.ai/v1/videos/upload` | [docs](https://docs.reka.ai/vision/api-reference/video-management/upload) |
| [Upload Video](actions/upload-video.md) | `POST https://vision-agent.api.reka.ai/v2/videos` | [docs](https://docs.reka.ai/vision/api-reference/v-2/upload-video-v-2-videos-post) |
