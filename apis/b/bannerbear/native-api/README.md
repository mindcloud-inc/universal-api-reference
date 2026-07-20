# Bannerbear: Native API Reference

A consolidated summary of Bannerbear's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://developers.bannerbear.com/
- **API base URL:** `https://api.bannerbear.com`

## Authentication

### API Key

Use a Bannerbear project API key in the Authorization bearer header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.bannerbear.com/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 25; maximum 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authorize](actions/authorize.md) | `GET /v2/auth` | [docs](https://developers.bannerbear.com/v2/#authentication) |
| [Create Collection](actions/create-collection.md) | `POST /v2/collections` | [docs](https://developers.bannerbear.com/v2/#collections) |
| [Create Image](actions/create-image.md) | `POST /v2/images` | [docs](https://developers.bannerbear.com/v2/#create-an-image) |
| [Create Movie](actions/create-movie.md) | `POST /v2/movies` | [docs](https://developers.bannerbear.com/v2/#create-a-movie) |
| [Create Template](actions/create-template.md) | `POST /v2/templates` | [docs](https://developers.bannerbear.com/v2/#create-a-template) |
| [Create Template Set](actions/create-template-set.md) | `POST /v2/template_sets` | [docs](https://developers.bannerbear.com/v2/#create-a-template-set) |
| [Create Video](actions/create-video.md) | `POST /v2/videos` | [docs](https://developers.bannerbear.com/v2/#create-a-video) |
| [Create Video Template](actions/create-video-template.md) | `POST /v2/video_templates` | [docs](https://developers.bannerbear.com/v2/#create-a-video-template) |
| [Delete Template](actions/delete-template.md) | `DELETE /v2/templates/:uid` | [docs](https://developers.bannerbear.com/v2/#delete-a-template) |
| [Duplicate Template](actions/duplicate-template.md) | `POST /v2/templates` | [docs](https://developers.bannerbear.com/v2/#duplicate-a-template) |
| [Get Account Usage](actions/get-account-usage.md) | `GET /v2/account` | [docs](https://developers.bannerbear.com/v2/#account) |
| [Get Collection](actions/get-collection.md) | `GET /v2/collections/:uid` | [docs](https://developers.bannerbear.com/v2/#collections) |
| [Get Image](actions/get-image.md) | `GET /v2/images/:uid` | [docs](https://developers.bannerbear.com/v2/#retrieve-an-image) |
| [Get Movie](actions/get-movie.md) | `GET /v2/movies/:uid` | [docs](https://developers.bannerbear.com/v2/#retrieve-a-movie) |
| [Get Template](actions/get-template.md) | `GET /v2/templates/:uid` | [docs](https://developers.bannerbear.com/v2/#retrieve-a-template) |
| [Get Template Set](actions/get-template-set.md) | `GET /v2/template_sets/:uid` | [docs](https://developers.bannerbear.com/v2/#retrieve-a-template-set) |
| [Get Video](actions/get-video.md) | `GET /v2/videos/:uid` | [docs](https://developers.bannerbear.com/v2/#retrieve-a-video) |
| [Get Video Template](actions/get-video-template.md) | `GET /v2/video_templates/:uid` | [docs](https://developers.bannerbear.com/v2/#retrieve-a-video-template) |
| [Import Templates](actions/import-templates.md) | `POST /v2/templates/import` | [docs](https://developers.bannerbear.com/v2/#import-templates) |
| [List Collections](actions/list-collections.md) | `GET /v2/collections` | [docs](https://developers.bannerbear.com/v2/#collections) |
| [List Images](actions/list-images.md) | `GET /v2/images` | [docs](https://developers.bannerbear.com/v2/#list-all-images) |
| [List Movies](actions/list-movies.md) | `GET /v2/movies` | [docs](https://developers.bannerbear.com/v2/#list-all-movies) |
| [List Template Sets](actions/list-template-sets.md) | `GET /v2/template_sets` | [docs](https://developers.bannerbear.com/v2/#list-all-template-sets) |
| [List Templates](actions/list-templates.md) | `GET /v2/templates` | [docs](https://developers.bannerbear.com/v2/#list-all-templates) |
| [List Video Templates](actions/list-video-templates.md) | `GET /v2/video_templates` | [docs](https://developers.bannerbear.com/v2/#list-all-video-templates) |
| [List Videos](actions/list-videos.md) | `GET /v2/videos` | [docs](https://developers.bannerbear.com/v2/#list-all-videos) |
| [Update Template](actions/update-template.md) | `PATCH /v2/templates/:uid` | [docs](https://developers.bannerbear.com/v2/#update-a-template) |
| [Update Template Set](actions/update-template-set.md) | `PATCH /v2/template_sets/:uid` | [docs](https://developers.bannerbear.com/v2/#update-a-template-set) |
| [Update Video](actions/update-video.md) | `PATCH /v2/videos` | [docs](https://developers.bannerbear.com/v2/#update-a-video) |
