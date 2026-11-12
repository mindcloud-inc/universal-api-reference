# Google Slides: Native API Reference

A consolidated summary of Google Slides's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://developers.google.com/workspace/slides/api/reference/rest
- **REST API base URL:** `https://slides.googleapis.com`
- **Google Drive API base URL:** `https://www.googleapis.com`
- **Google OpenID Connect base URL:** `https://openidconnect.googleapis.com`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.google.com/o/oauth2/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.googleapis.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `https://www.googleapis.com/auth/drive.file openid https://www.googleapis.com/auth/userinfo.email https://www.googleapis.com/auth/userinfo.profile`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://oauth2.googleapis.com/token.

[Official authentication documentation](https://developers.google.com/identity/protocols/oauth2)

## API conventions

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

### Google Drive API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `nextPageToken`.

### Google OpenID Connect

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

- **Google Drive API:** Use `pageSize` in the query string to set the page size (default 1000; accepted range 1–1000). Use `pageToken` in the query string as the pagination cursor.

## Endpoints (21 documented)

| Operation | API | Method & path | Vendor docs |
| --- | --- | --- | --- |
| [Batch Update Presentation](actions/batch-update-presentation.md) | rest | `POST /v1/presentations/[:presentationId]\:batchUpdate` | [docs](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/batchUpdate) |
| [Copy Presentation](actions/copy-presentation.md) | Google Drive API | `POST /drive/v3/files/:fileId/copy` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/copy) |
| [Create Image](actions/create-image.md) | rest | `POST /v1/presentations/[:presentationId]\:batchUpdate` | [docs](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/request#CreateImageRequest) |
| [Create Presentation](actions/create-presentation.md) | rest | `POST /v1/presentations` | [docs](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/create) |
| [Create Shape](actions/create-shape.md) | rest | `POST /v1/presentations/[:presentationId]\:batchUpdate` | [docs](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/request#CreateShapeRequest) |
| [Create Slide](actions/create-slide.md) | rest | `POST /v1/presentations/[:presentationId]\:batchUpdate` | [docs](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/request#CreateSlideRequest) |
| [Create Table](actions/create-table.md) | rest | `POST /v1/presentations/[:presentationId]\:batchUpdate` | [docs](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/request#CreateTableRequest) |
| [Delete Object](actions/delete-object.md) | rest | `POST /v1/presentations/[:presentationId]\:batchUpdate` | [docs](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/request#DeleteObjectRequest) |
| [Delete Presentation](actions/delete-presentation.md) | Google Drive API | `DELETE /drive/v3/files/:fileId` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/delete) |
| [Delete Text](actions/delete-text.md) | rest | `POST /v1/presentations/[:presentationId]\:batchUpdate` | [docs](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/request#DeleteTextRequest) |
| [Duplicate Object](actions/duplicate-object.md) | rest | `POST /v1/presentations/[:presentationId]\:batchUpdate` | [docs](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/request#DuplicateObjectRequest) |
| [Get Current User](actions/get-current-user.md) | Google OpenID Connect | `GET /v1/userinfo` | [docs](https://developers.google.com/identity/openid-connect/openid-connect) |
| [Get Page](actions/get-page.md) | rest | `GET /v1/presentations/:presentationId/pages/:pageObjectId` | [docs](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations.pages/get) |
| [Get Page Thumbnail](actions/get-page-thumbnail.md) | rest | `GET /v1/presentations/:presentationId/pages/:pageObjectId/thumbnail` | [docs](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations.pages/getThumbnail) |
| [Get Presentation](actions/get-presentation.md) | rest | `GET /v1/presentations/:presentationId` | [docs](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/get) |
| [Insert Text](actions/insert-text.md) | rest | `POST /v1/presentations/[:presentationId]\:batchUpdate` | [docs](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/request#InsertTextRequest) |
| [List Presentations](actions/list-presentations.md) | Google Drive API | `GET /drive/v3/files` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/list) |
| [Replace All Shapes with Image](actions/replace-all-shapes-with-image.md) | rest | `POST /v1/presentations/[:presentationId]\:batchUpdate` | [docs](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/request#ReplaceAllShapesWithImageRequest) |
| [Replace All Text](actions/replace-all-text.md) | rest | `POST /v1/presentations/[:presentationId]\:batchUpdate` | [docs](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/request#ReplaceAllTextRequest) |
| [Update Presentation](actions/update-presentation.md) | Google Drive API | `PATCH /drive/v3/files/:fileId` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/update) |
| [Update Slides Position](actions/update-slides-position.md) | rest | `POST /v1/presentations/[:presentationId]\:batchUpdate` | [docs](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/request#UpdateSlidesPositionRequest) |
