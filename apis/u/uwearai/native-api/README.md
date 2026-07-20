# Uwear.ai: Native API Reference

A consolidated summary of Uwear.ai's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://docs.dev.uwear.ai/
- **API base URL:** `https://api.uwear.ai`

## Authentication

### API Key

Use your Uwear.ai API key with bearer authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.dev.uwear.ai/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `items_per_page` in the query string to set the page size (default 20; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Avatar](actions/create-avatar.md) | `POST /api/v1/generation-avatar` | [docs](https://docs.dev.uwear.ai/operations/external_avatar_generation) |
| [Create Edit](actions/create-edit.md) | `POST /api/v1/generation-edit` | [docs](https://docs.dev.uwear.ai/operations/external_edit_generation) |
| [Create Generation](actions/create-generation.md) | `POST /api/v1/generation` | [docs](https://docs.dev.uwear.ai/operations/external_create_generation) |
| [Create New Clothing Item](actions/create-new-clothing-item.md) | `POST /api/v1/clothing-item` | [docs](https://docs.dev.uwear.ai/operations/external_create_clothing_item) |
| [Create Upscale](actions/create-upscale.md) | `POST /api/v1/generation-upscale` | [docs](https://docs.dev.uwear.ai/operations/external_upscale_generation) |
| [Create Video](actions/create-video.md) | `POST /api/v1/generation-video` | [docs](https://docs.dev.uwear.ai/operations/external_video_generation) |
| [Delete Avatar](actions/delete-avatar.md) | `DELETE /api/v1/avatar/:avatar_id` | [docs](https://docs.dev.uwear.ai/operations/external_delete_avatar) |
| [Delete Clothing Item](actions/delete-clothing-item.md) | `DELETE /api/v1/clothing-item/:clothing_item_id` | [docs](https://docs.dev.uwear.ai/operations/external_delete_clothing_item) |
| [Get All Avatars](actions/get-all-avatars.md) | `GET /api/v1/avatars` | [docs](https://docs.dev.uwear.ai/operations/external_read_avatars) |
| [Get All Clothing Items](actions/get-all-clothing-items.md) | `GET /api/v1/clothing-items` | [docs](https://docs.dev.uwear.ai/operations/external_read_clothing_items) |
| [Get All Generation Results](actions/get-all-generation-results.md) | `GET /api/v1/generation-results` | [docs](https://docs.dev.uwear.ai/operations/external_read_generation_results) |
| [Get All Generations](actions/get-all-generations.md) | `GET /api/v1/generations` | [docs](https://docs.dev.uwear.ai/operations/external_read_generations) |
| [Get Avatar Details](actions/get-avatar-details.md) | `GET /api/v1/avatar/:avatar_id` | [docs](https://docs.dev.uwear.ai/operations/external_read_avatar) |
| [Get Clothing Item Details](actions/get-clothing-item-details.md) | `GET /api/v1/clothing-item/:clothing_item_id` | [docs](https://docs.dev.uwear.ai/operations/external_read_clothing_item) |
| [Get Generation Details](actions/get-generation-details.md) | `GET /api/v1/generation/:generation_id` | [docs](https://docs.dev.uwear.ai/operations/external_read_generation) |
| [Get Generation Result Details](actions/get-generation-result-details.md) | `GET /api/v1/generation-result/:generation_result_id` | [docs](https://docs.dev.uwear.ai/operations/external_read_generation_result) |
| [Save Avatar](actions/save-avatar.md) | `POST /api/v1/avatar` | [docs](https://docs.dev.uwear.ai/operations/external_create_avatar) |
| [Update Avatar](actions/update-avatar.md) | `PUT /api/v1/avatar/:avatar_id` | [docs](https://docs.dev.uwear.ai/operations/external_update_avatar) |
| [Update Clothing Item](actions/update-clothing-item.md) | `PUT /api/v1/clothing-item/:clothing_item_id` | [docs](https://docs.dev.uwear.ai/operations/external_update_clothing_item) |
