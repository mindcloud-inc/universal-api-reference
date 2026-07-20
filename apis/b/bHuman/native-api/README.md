# BHuman: Native API Reference

A consolidated summary of BHuman's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://github.com/bhuman-ai/public_api
- **API base URL:** `https://studio.bhuman.ai/api`

## Authentication

### API Credential

Use this auth. Enter your BHuman `client_id:client_secret` as a single value.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://github.com/bhuman-ai/public_api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `size` in the query string to set the page size (default 100; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Video by Campaign](actions/generate-video-by-campaign.md) | `POST /ai_studio/pipeline/campaign` | [docs](https://github.com/bhuman-ai/public_api#api-endpoints) |
| [Generate Video by Instance](actions/generate-video-by-instance.md) | `POST /ai_studio/try_sample` | [docs](https://github.com/bhuman-ai/public_api#api-endpoints) |
| [Get Generated Video](actions/get-generated-video.md) | `GET /ai_studio/generated_video_by_id` | [docs](https://github.com/bhuman-ai/public_api#api-endpoints) |
| [Get Store Settings](actions/get-store-settings.md) | `GET https://store.bhuman.ai/api/store/settings` | [docs](https://github.com/bhuman-ai/public_api#api-endpoints) |
| [Get Video Instance](actions/get-video-instance.md) | `GET /ai_studio/video_instance` | [docs](https://github.com/bhuman-ai/public_api#api-endpoints) |
| [List Generated Videos by Campaign](actions/list-generated-videos-by-campaign.md) | `GET /ai_studio/generated_video_by_campaign_id` | [docs](https://github.com/bhuman-ai/public_api#api-endpoints) |
| [List Generated Videos by Instance](actions/list-generated-videos-by-instance.md) | `GET /ai_studio/generated_video_by_video_instance_id` | [docs](https://github.com/bhuman-ai/public_api#api-endpoints) |
| [List Store Products](actions/list-store-products.md) | `GET https://store.bhuman.ai/api/store/product` | [docs](https://github.com/bhuman-ai/public_api#api-endpoints) |
| [List Video Instances](actions/list-video-instances.md) | `GET /ai_studio/video_instances` | [docs](https://github.com/bhuman-ai/public_api) |
| [List Workspaces](actions/list-workspaces.md) | `GET https://user.bhuman.ai/api/workspace` | [docs](https://github.com/bhuman-ai/public_api) |
| [Use Store Product](actions/use-store-product.md) | `POST https://store.bhuman.ai/api/store/product/use` | [docs](https://github.com/bhuman-ai/public_api#api-endpoints) |
