# Google Slides: Native API Reference

A consolidated summary of Google Slides's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://developers.google.com/workspace/slides/api/reference/rest
- **API base URL:** `https://slides.googleapis.com`

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

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Presentation](actions/create-presentation.md) | `POST /v1/presentations` | [docs](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/create) |
| [Delete Presentation](actions/delete-presentation.md) | `DELETE https://www.googleapis.com/drive/v3/files/:fileId` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/delete) |
| [Get Page](actions/get-page.md) | `GET /v1/presentations/:presentationId/pages/:pageObjectId` | [docs](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations.pages/get) |
| [Get Page Thumbnail](actions/get-page-thumbnail.md) | `GET /v1/presentations/:presentationId/pages/:pageObjectId/thumbnail` | [docs](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations.pages/getThumbnail) |
| [Get Presentation](actions/get-presentation.md) | `GET /v1/presentations/:presentationId` | [docs](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/get) |
| [Update Presentation](actions/update-presentation.md) | `PATCH https://www.googleapis.com/drive/v3/files/:fileId` | [docs](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/update) |
