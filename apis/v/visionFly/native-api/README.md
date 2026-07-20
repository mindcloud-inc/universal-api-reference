# VisionFly: Native API Reference

A consolidated summary of VisionFly's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://api.visionfly.ai/docs
- **OpenAPI specification:** https://api.visionfly.ai/openapi.json
- **API base URL:** `https://api.visionfly.ai`

## Authentication

### API Key

Use your VisionFly API key from the VisionFly dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.visionfly.ai/api-reference/introduction)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Image from CDN](actions/delete-image-from-cdn.md) | `DELETE /cdn/:image_id` | [docs](https://api.visionfly.ai/docs#/default/delete_single_image_cdn__image_id__delete) |
| [Delete Multiple Images](actions/delete-multiple-images.md) | `DELETE /cdn/images` | [docs](https://api.visionfly.ai/docs#/default/delete_images_cdn_images_delete) |
| [Get Passport Photo Specifications](actions/get-passport-photo-specifications.md) | `GET /passport-photo/specs` | [docs](https://api.visionfly.ai/docs#/default/get_passport_specs_passport_photo_specs_get) |
| [Get Plans](actions/get-plans.md) | `GET /plans` | [docs](https://api.visionfly.ai/docs#/default/get_plans_plans_get) |
| [Get Root Info](actions/get-root-info.md) | `GET /` | [docs](https://api.visionfly.ai/docs#/default/root__get) |
| [Get Usage Statistics](actions/get-usage-statistics.md) | `GET /cdn/usage` | [docs](https://api.visionfly.ai/docs#/default/get_usage_cdn_usage_get) |
| [Health Check](actions/health-check.md) | `GET /health` | [docs](https://api.visionfly.ai/docs#/default/health_check_health_get) |
| [List Projects](actions/list-projects.md) | `GET /cdn/projects` | [docs](https://api.visionfly.ai/docs#/default/list_projects_cdn_projects_get) |
| [List User Images](actions/list-user-images.md) | `GET /cdn/images` | [docs](https://api.visionfly.ai/docs#/default/list_images_cdn_images_get) |
| [Serve CDN Image](actions/serve-cdn-image.md) | `GET /cdn/:image_id` | [docs](https://api.visionfly.ai/docs#/default/serve_image_cdn__image_id__get) |
| [Test API Key](actions/test-api-key.md) | `GET /image/test` | [docs](https://api.visionfly.ai/docs#/default/test_authentication_image_test_get) |
| [Upload Image to CDN](actions/upload-image-to-cdn.md) | `POST /cdn/upload` | [docs](https://api.visionfly.ai/docs#/default/upload_image_cdn_upload_post) |
