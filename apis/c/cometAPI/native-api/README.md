# CometAPI: Native API Reference

A consolidated summary of CometAPI's API configuration and 86 documented operations, with links to official documentation.

- **Official docs:** https://www.cometapi.com/how-to-use-cometapi-a-beginners-guide/
- **API base URL:** `https://api.cometapi.com`

## Authentication

### API Key

Store one CometAPI API key and inject it per API family: bearer for OpenAI-compatible routes, x-api-key for Anthropic-compatible routes, and x-goog-api-key for Gemini-compatible routes.

### Credentials

- **API Key:** `apiKey` · required · CometAPI API key from the CometAPI console.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
x-api-key: <apiKey>
x-goog-api-key: <apiKey>
```

[Official authentication documentation](https://www.cometapi.com/how-to-use-cometapi-a-beginners-guide/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (86 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bria Edit Image](actions/bria-edit-image.md) | `POST /bria/image/edit/:action` | [docs](https://apidoc.cometapi.com/api/image/bria/image-editing) |
| [Bria Generate Image](actions/bria-generate-image.md) | `POST /bria/text-to-image` | [docs](https://apidoc.cometapi.com/api/image/bria/generate-image) |
| [Bria Generate Vector](actions/bria-generate-vector.md) | `POST /bria/text-to-vector` | [docs](https://apidoc.cometapi.com/api/image/bria/generate-vector-graphics-base) |
| [Bria Get Request](actions/bria-get-request.md) | `GET /bria/:request_id` | [docs](https://apidoc.cometapi.com/api/image/bria/query-status) |
| [Bytedance Image Edit](actions/bytedance-image-edit.md) | `POST /v1/images/edits` | [docs](https://apidoc.cometapi.com/api/image/seededit-seedream/bytedance-image-editing) |
| [Bytedance Video Create](actions/bytedance-video-create.md) | `POST /volc/v3/contents/generations/tasks` | [docs](https://apidoc.cometapi.com/api/video/bytedance/bytedance-video) |
| [Bytedance Video Get](actions/bytedance-video-get.md) | `GET /volc/v3/contents/generations/tasks/:id` | [docs](https://apidoc.cometapi.com/api/video/bytedance/bytedance-video-get) |
| [Cancel Message Batch](actions/cancel-message-batch.md) | `POST /v1/messages/batches/:message_batch_id/cancel` | [docs](https://www.cometapi.com/claude-opus-4-5-api/) |
| [Count Message Tokens](actions/count-message-tokens.md) | `POST /v1/messages/count_tokens` | [docs](https://www.cometapi.com/claude-opus-4-5-api/) |
| [Create Chat Completion](actions/create-chat-completion.md) | `POST /v1/chat/completions` | [docs](https://www.cometapi.com/how-to-use-cometapi-a-beginners-guide/) |
| [Create Embedding](actions/create-embedding.md) | `POST /v1/embeddings` | [docs](https://www.cometapi.com/how-to-use-cometapi-a-beginners-guide/) |
| [Create Image Generation](actions/create-image-generation.md) | `POST /v1/images/generations` | [docs](https://www.cometapi.com/how-to-use-cometapi-a-beginners-guide/) |
| [Create Message](actions/create-message.md) | `POST /v1/messages` | [docs](https://www.cometapi.com/claude-opus-4-5-api/) |
| [Create Message Batch](actions/create-message-batch.md) | `POST /v1/messages/batches` | [docs](https://www.cometapi.com/claude-opus-4-5-api/) |
| [Create Moderation](actions/create-moderation.md) | `POST /v1/moderations` | [docs](https://www.cometapi.com/how-to-use-cometapi-a-beginners-guide/) |
| [Create Response](actions/create-response.md) | `POST /v1/responses` | [docs](https://www.cometapi.com/how-to-use-cometapi-a-beginners-guide/) |
| [Create Speech](actions/create-speech.md) | `POST /v1/audio/speech` | [docs](https://www.cometapi.com/how-to-use-cometapi-a-beginners-guide/) |
| [Create Transcription](actions/create-transcription.md) | `POST /v1/audio/transcriptions` | [docs](https://www.cometapi.com/how-to-use-cometapi-a-beginners-guide/) |
| [Create Translation](actions/create-translation.md) | `POST /v1/audio/translations` | [docs](https://www.cometapi.com/how-to-use-cometapi-a-beginners-guide/) |
| [Delete Message Batch](actions/delete-message-batch.md) | `DELETE /v1/messages/batches/:message_batch_id` | [docs](https://www.cometapi.com/claude-opus-4-5-api/) |
| [Delete Model](actions/delete-model.md) | `DELETE /v1/models/:model_id` | [docs](https://www.cometapi.com/how-to-use-cometapi-a-beginners-guide/) |
| [Flux Generate Image](actions/flux-generate-image.md) | `POST /flux/v1/:model` | [docs](https://apidoc.cometapi.com/api/image/flux/flux-generate-image) |
| [Flux Get Result](actions/flux-get-result.md) | `GET /flux/v1/get_result` | [docs](https://apidoc.cometapi.com/api/image/flux/flux-query) |
| [Generate Content](actions/generate-content.md) | `POST /v1beta/models/:model` | [docs](https://www.cometapi.com/how-to-use-ai-api-via-cometapi/) |
| [Get Message Batch](actions/get-message-batch.md) | `GET /v1/messages/batches/:message_batch_id` | [docs](https://www.cometapi.com/claude-opus-4-5-api/) |
| [Get Message Batch Results](actions/get-message-batch-results.md) | `GET /v1/messages/batches/:message_batch_id/results` | [docs](https://www.cometapi.com/claude-opus-4-5-api/) |
| [Get Model](actions/get-model.md) | `GET /v1/models/:model_id` | [docs](https://www.cometapi.com/how-to-use-cometapi-a-beginners-guide/) |
| [Kling Add Video Selection](actions/kling-add-video-selection.md) | `POST /kling/v1/videos/multi-elements/add-selection` | [docs](https://apidoc.cometapi.com/api/video/kling/multimodal-video-editing/add-video-selection) |
| [Kling Advanced Lip Sync](actions/kling-advanced-lip-sync.md) | `POST /kling/v1/videos/advanced-lip-sync` | [docs](https://apidoc.cometapi.com/api/video/kling/counterpart-creating-tasks) |
| [Kling Avatar Image To Video](actions/kling-avatar-image-to-video.md) | `POST /kling/v1/videos/avatar/image2video` | [docs](https://apidoc.cometapi.com/api/video/kling/avatar) |
| [Kling Clear Video Selection](actions/kling-clear-video-selection.md) | `POST /kling/v1/videos/multi-elements/clear-selection` | [docs](https://apidoc.cometapi.com/api/video/kling/multimodal-video-editing/clear-video-selection) |
| [Kling Create Video Edit Task](actions/kling-create-video-edit-task.md) | `POST /kling/v1/videos/multi-elements` | [docs](https://apidoc.cometapi.com/api/video/kling/multimodal-video-editing/create-task) |
| [Kling Delete Video Selection](actions/kling-delete-video-selection.md) | `POST /kling/v1/videos/multi-elements/delete-selection` | [docs](https://apidoc.cometapi.com/api/video/kling/multimodal-video-editing/delete-video-selection) |
| [Kling Identify Face](actions/kling-identify-face.md) | `POST /kling/v1/videos/identify-face` | [docs](https://apidoc.cometapi.com/api/video/kling/lip-sync) |
| [Kling Image Expansion](actions/kling-image-expansion.md) | `POST /kling/v1/images/editing/expand` | [docs](https://apidoc.cometapi.com/api/video/kling/image-expansion) |
| [Kling Image Generation](actions/kling-image-generation.md) | `POST /kling/v1/images/generations` | [docs](https://apidoc.cometapi.com/api/video/kling/image-generation) |
| [Kling Image Recognize](actions/kling-image-recognize.md) | `POST /kling/v1/videos/image-recognize` | [docs](https://apidoc.cometapi.com/api/video/kling/image-recognize) |
| [Kling Image To Video](actions/kling-image-to-video.md) | `POST /kling/v1/videos/image2video` | [docs](https://apidoc.cometapi.com/api/video/kling/image-to-video) |
| [Kling Individual Query](actions/kling-individual-query.md) | `GET /kling/v1/:action/:action2/:task_id` | [docs](https://apidoc.cometapi.com/api/video/kling/individual-queries) |
| [Kling Initialize Video Editing](actions/kling-initialize-video-editing.md) | `POST /kling/v1/videos/multi-elements/init-selection` | [docs](https://apidoc.cometapi.com/api/video/kling/multimodal-video-editing/initialize-video-for-editing) |
| [Kling Multi Image To Image](actions/kling-multi-image-to-image.md) | `POST /kling/v1/images/generations` | [docs](https://apidoc.cometapi.com/api/video/kling/multi-image-to-image) |
| [Kling Multi Image To Video](actions/kling-multi-image-to-video.md) | `POST /kling/v1/videos/multi-image2video` | [docs](https://apidoc.cometapi.com/api/video/kling/multi-image-to-video) |
| [Kling Omni Query](actions/kling-omni-query.md) | `GET /kling/v1/videos/omni-video/:task_id` | [docs](https://apidoc.cometapi.com/api/video/kling/omni-query) |
| [Kling Omni Video](actions/kling-omni-video.md) | `POST /kling/v1/videos/omni-video` | [docs](https://apidoc.cometapi.com/api/video/kling/omni-video) |
| [Kling Preview Video Selection](actions/kling-preview-video-selection.md) | `POST /kling/v1/videos/multi-elements/preview-selection` | [docs](https://apidoc.cometapi.com/api/video/kling/multimodal-video-editing/preview-selected-video-area) |
| [Kling Text To Audio](actions/kling-text-to-audio.md) | `POST /kling/v1/audio/text-to-audio` | [docs](https://apidoc.cometapi.com/api/video/kling/text-to-audio) |
| [Kling Text To Video](actions/kling-text-to-video.md) | `POST /kling/v1/videos/text2video` | [docs](https://apidoc.cometapi.com/api/video/kling/text-to-video) |
| [Kling TTS](actions/kling-tts.md) | `POST /kling/v1/audio/tts` | [docs](https://apidoc.cometapi.com/api/video/kling/tts) |
| [Kling Video Effects](actions/kling-video-effects.md) | `POST /kling/v1/videos/effects` | [docs](https://apidoc.cometapi.com/api/video/kling/video-effects) |
| [Kling Video Extension](actions/kling-video-extension.md) | `POST /kling/v1/videos/video-extend` | [docs](https://apidoc.cometapi.com/api/video/kling/video-extension) |
| [Kling Video To Audio](actions/kling-video-to-audio.md) | `POST /kling/v1/audio/video-to-audio` | [docs](https://apidoc.cometapi.com/api/video/kling/video-to-audio) |
| [Kling Virtual Try On](actions/kling-virtual-try-on.md) | `POST /kling/v1/images/kolors-virtual-try-on` | [docs](https://apidoc.cometapi.com/api/video/kling/virtual-try-on) |
| [List Files](actions/list-files-restored.md) | `GET /v1/files` | [docs](https://www.cometapi.com/how-to-use-cometapi-a-beginners-guide/) |
| [List Message Batches](actions/list-message-batches.md) | `GET /v1/messages/batches` | [docs](https://www.cometapi.com/claude-opus-4-5-api/) |
| [List Models](actions/list-models.md) | `GET /v1/models` | [docs](https://www.cometapi.com/how-to-use-cometapi-a-beginners-guide/) |
| [Midjourney Blend](actions/midjourney-blend.md) | `POST /mj/submit/blend` | [docs](https://apidoc.cometapi.com/api/image/midjourney/blend) |
| [Midjourney Describe](actions/midjourney-describe.md) | `POST /mj/submit/describe` | [docs](https://apidoc.cometapi.com/api/image/midjourney/describe) |
| [Midjourney Get Task](actions/midjourney-get-task.md) | `GET /mj/task/:id/fetch` | [docs](https://apidoc.cometapi.com/api/image/midjourney/task-fetching-api/fetch-single-task) |
| [Midjourney Imagine](actions/midjourney-imagine.md) | `POST /mj/submit/imagine` | [docs](https://apidoc.cometapi.com/api/image/midjourney/imagine) |
| [Midjourney List Tasks](actions/midjourney-list-tasks.md) | `POST /mj/task/list-by-condition` | [docs](https://apidoc.cometapi.com/api/image/midjourney/task-fetching-api/list-by-condition) |
| [Midjourney Modal](actions/midjourney-modal.md) | `POST /mj/submit/modal` | [docs](https://apidoc.cometapi.com/api/image/midjourney/modal) |
| [Midjourney Submit Action](actions/midjourney-submit-action.md) | `POST /mj/submit/action` | [docs](https://apidoc.cometapi.com/api/image/midjourney/action) |
| [Midjourney Submit Editor](actions/midjourney-submit-editor.md) | `POST /mj/submit/edits` | [docs](https://apidoc.cometapi.com/api/image/midjourney/submit-editor) |
| [Midjourney Submit Video](actions/midjourney-submit-video.md) | `POST /mj/submit/video` | [docs](https://apidoc.cometapi.com/api/image/midjourney/submit-video) |
| [OpenAI Image Edit](actions/openai-image-edit.md) | `POST /v1/images/edits` | [docs](https://apidoc.cometapi.com/api/image/openai/image-editing) |
| [Replicate Create Prediction](actions/replicate-create-prediction.md) | `POST /replicate/v1/models/:models/predictions` | [docs](https://apidoc.cometapi.com/api/image/replicate/create-predictions-general) |
| [Replicate Get Prediction](actions/replicate-get-prediction.md) | `GET /replicate/v1/predictions/:id` | [docs](https://apidoc.cometapi.com/api/image/replicate/replicate-query) |
| [Runway Act One](actions/runway-act-one.md) | `POST /runway/pro/act_one` | [docs](https://apidoc.cometapi.com/api/video/runway/reverse-format/act-one-expression-migration) |
| [Runway Character Performance](actions/runway-character-performance.md) | `POST /runwayml/v1/character_performance` | [docs](https://apidoc.cometapi.com/api/video/runway/official-format/control-a-character) |
| [Runway Feed Get Task](actions/runway-feed-get-task.md) | `POST /runway/feed` | [docs](https://apidoc.cometapi.com/api/video/runway/reverse-format/feed-get-task) |
| [Runway Generate](actions/runway-generate.md) | `POST /runway/pro/generate` | [docs](https://apidoc.cometapi.com/api/video/runway/reverse-format/generate) |
| [Runway Generate Image To Video](actions/runway-generate-image-to-video.md) | `POST /runway/pro/generate` | [docs](https://apidoc.cometapi.com/api/video/runway/reverse-format/image-to-video) |
| [Runway Get Task](actions/runway-get-task.md) | `GET /runwayml/v1/tasks/:id` | [docs](https://apidoc.cometapi.com/api/video/runway/official-format/runway-to-get-task-details) |
| [Runway Image To Video](actions/runway-image-to-video.md) | `POST /runwayml/v1/image_to_video` | [docs](https://apidoc.cometapi.com/api/video/runway/official-format/runway-images-raw-video) |
| [Runway Video To Video](actions/runway-video-to-video.md) | `POST /runwayml/v1/video_to_video` | [docs](https://apidoc.cometapi.com/api/video/runway/official-format/generate-a-video-from-a-video) |
| [Runway Video Upscale](actions/runway-video-upscale.md) | `POST /runwayml/v1/video_upscale` | [docs](https://apidoc.cometapi.com/api/video/runway/official-format/upscale-a-video) |
| [Runway Video2Video Style Redraw](actions/runway-video2video-style-redraw.md) | `POST /runway/pro/video2video` | [docs](https://apidoc.cometapi.com/api/video/runway/reverse-format/video-to-video-style-redraw) |
| [Sora Create Video](actions/sora-create-video.md) | `POST /v1/videos` | [docs](https://apidoc.cometapi.com/api/video/sora-2/official/create-video) |
| [Sora Get Video](actions/sora-get-video.md) | `GET /v1/videos/:video_id` | [docs](https://apidoc.cometapi.com/api/video/sora-2/official/retrieve-video) |
| [Sora Get Video Content](actions/sora-get-video-content.md) | `GET /v1/videos/:video_id/content` | [docs](https://apidoc.cometapi.com/api/video/sora-2/official/retrieve-video-content) |
| [Sora Remix Video](actions/sora-remix-video.md) | `POST /v1/videos/:video_id/remix` | [docs](https://apidoc.cometapi.com/api/video/sora-2/official/remix-video) |
| [Veo3 Create Video](actions/veo3-create-video.md) | `POST /v1/videos` | [docs](https://apidoc.cometapi.com/api/video/veo3/self-developed/veo3-async-generation) |
| [Veo3 Get Video](actions/veo3-get-video.md) | `GET /v1/videos/:video_id` | [docs](https://apidoc.cometapi.com/api/video/veo3/self-developed/veo3-retrive) |
| [xAI Get Video Result](actions/xai-get-video-result.md) | `GET /grok/v1/videos/:request_id` | [docs](https://apidoc.cometapi.com/api/video/xai/get-video-generation-results) |
| [xAI Video Edit](actions/xai-video-edit.md) | `POST /grok/v1/videos/edits` | [docs](https://apidoc.cometapi.com/api/video/xai/video-edit) |
| [xAI Video Generation](actions/xai-video-generation.md) | `POST /grok/v1/videos/generations` | [docs](https://apidoc.cometapi.com/api/video/xai/video-generation) |
