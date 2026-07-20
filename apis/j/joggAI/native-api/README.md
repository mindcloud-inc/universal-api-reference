# JoggAI: Native API Reference

A consolidated summary of JoggAI's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://docs.jogg.ai/api-reference/v2/QuickStart/GettingStarted
- **API base URL:** `https://api.jogg.ai`

## Authentication

### API Key

Use your JoggAI API key from the API menu.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.jogg.ai/api-reference/v2/QuickStart/GettingStarted)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `data.pagination.total_pages`. The current page number is read from `data.pagination.page`.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Lip Sync Video Task](actions/create-lip-sync-video-task.md) | `POST /v2/create_lip_sync_video` | [docs](https://docs.jogg.ai/api-reference/v2/Video/CreateLipSyncVideo) |
| [Create Photo Avatar](actions/create-photo-avatar.md) | `POST /v2/photo_avatar/photo/generate` | [docs](https://docs.jogg.ai/api-reference/v2/Avatar/PhotoAvatarGenerate) |
| [Create Product](actions/create-product.md) | `POST /v2/product` | [docs](https://docs.jogg.ai/api-reference/v2/Product/CreateProduct) |
| [Create Video From Avatar](actions/create-video-from-avatar.md) | `POST /v2/create_video_from_avatar` | [docs](https://docs.jogg.ai/api-reference/v2/API%20Documentation/CreateAvatarVideos) |
| [Create Video From Product](actions/create-video-from-product.md) | `POST /v2/create_video_from_product` | [docs](https://docs.jogg.ai/api-reference/v2/Video/CreateVideoFromProduct) |
| [Create Video with Template](actions/create-video-with-template.md) | `POST /v2/create_video_with_template` | [docs](https://docs.jogg.ai/api-reference/v2/Video/CreateVideoWithTemplate) |
| [Create Webhook Endpoint](actions/create-webhook-endpoint.md) | `POST /v2/endpoint` | [docs](https://docs.jogg.ai/api-reference/v2/Webhook/AddWebhookEndpoint) |
| [Delete Webhook Endpoint](actions/delete-webhook-endpoint.md) | `DELETE /v2/endpoint/{endpointId}` | [docs](https://docs.jogg.ai/api-reference/v2/Webhook/DeleteWebhookEndpoint) |
| [Generate AI Scripts](actions/generate-ai-scripts.md) | `POST /v2/ai_scripts` | [docs](https://docs.jogg.ai/api-reference/v2/Asset/CreateAIScript) |
| [Get AI Script Results](actions/get-ai-script-results.md) | `GET /v2/ai_scripts/results/{taskId}` | [docs](https://docs.jogg.ai/api-reference/v2/Asset/GetAIScriptResult) |
| [Get Avatar Video Status](actions/get-avatar-video-status.md) | `GET /v2/avatar_video/{videoId}` | [docs](https://docs.jogg.ai/api-reference/v2/Video/AvatarVideoGet) |
| [Get Motion Status](actions/get-motion-status.md) | `GET /v2/photo_avatar` | [docs](https://docs.jogg.ai/api-reference/v2/Avatar/MotionStatusCheck) |
| [Get Photo Avatar Status](actions/get-photo-avatar-status.md) | `GET /v2/photo_avatar/photo` | [docs](https://docs.jogg.ai/api-reference/v2/Avatar/PhotoAvatarStatusGet) |
| [Get Remaining Quota](actions/get-remaining-quota.md) | `GET /v2/user/remaining_quota` | [docs](https://docs.jogg.ai/api-reference/v2/User/GetRemainingQuota) |
| [Get Template](actions/get-template.md) | `GET /v2/template/custom/{id}` | [docs](https://docs.jogg.ai/api-reference/v2/Template/GetTemplateById) |
| [Get Template Video](actions/get-template-video.md) | `GET /v2/template_video/{videoId}` | [docs](https://docs.jogg.ai/api-reference/v2/Video/TemplateVideoGet) |
| [Get Translation Status](actions/get-translation-status.md) | `GET /v2/video_translate/{videoTranslateId}` | [docs](https://docs.jogg.ai/api-reference/v2/API%20Documentation/VideoTranslation) |
| [Get User Info](actions/get-user-info.md) | `GET /v2/user/whoami` | [docs](https://docs.jogg.ai/api-reference/v2/User/GetUserInfo) |
| [List Background Music](actions/list-background-music.md) | `GET /v2/musics` | [docs](https://docs.jogg.ai/api-reference/v2/Asset/GetMusic) |
| [List Custom Avatars](actions/list-custom-avatars.md) | `GET /v2/avatars/custom` | [docs](https://docs.jogg.ai/api-reference/v2/Avatar/CustomAvatarsGet) |
| [List Custom Voices](actions/list-custom-voices.md) | `GET /v2/voices/custom` | [docs](https://docs.jogg.ai/api-reference/v2/Voice/GetCustomVoices) |
| [List Photo Avatars](actions/list-photo-avatars.md) | `GET /v2/avatars/photo_avatars` | [docs](https://docs.jogg.ai/api-reference/v2/Avatar/PhotoAvatarsGet) |
| [List Public Avatars](actions/list-public-avatars.md) | `GET /v2/avatars/public` | [docs](https://docs.jogg.ai/api-reference/v2/Avatar/PublicAvatarsGet) |
| [List Templates](actions/list-templates.md) | `GET /v2/templates/custom` | [docs](https://docs.jogg.ai/api-reference/v2/Template/GetTemplates) |
| [List Translation Target Languages](actions/list-translation-target-languages.md) | `GET /v2/video_translate/target_languages` | [docs](https://docs.jogg.ai/api-reference/v2/Video/VideoTranslateTargetLanguagesList) |
| [List Visual Styles](actions/list-visual-styles.md) | `GET /v2/visual_styles` | [docs](https://docs.jogg.ai/api-reference/v2/Asset/GetVisualStyles) |
| [List Voices](actions/list-voices.md) | `GET /v2/voices` | [docs](https://docs.jogg.ai/api-reference/v2/Voice/GetVoices) |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | `GET /v2/endpoints` | [docs](https://docs.jogg.ai/api-reference/v2/Webhook/ListWebhookEndpoints) |
| [List Webhook Events](actions/list-webhook-events.md) | `GET /v2/events` | [docs](https://docs.jogg.ai/api-reference/v2/Webhook/ListWebhookEvents) |
| [Translate Video](actions/translate-video.md) | `POST /v2/video_translate/` | [docs](https://docs.jogg.ai/api-reference/v2/Video/VideoTranslateCreate) |
| [Update Product](actions/update-product.md) | `PUT /v2/product` | [docs](https://docs.jogg.ai/api-reference/v2/Product/UpdateProduct) |
| [Upload Asset](actions/upload-asset.md) | `POST /v2/upload/asset` | [docs](https://docs.jogg.ai/api-reference/v2/Asset/UploadAsset) |
