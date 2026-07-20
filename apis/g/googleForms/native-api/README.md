# Google Forms: Native API Reference

A consolidated summary of Google Forms's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://developers.google.com/workspace/forms/api/reference/rest
- **OpenAPI specification:** https://forms.googleapis.com/$discovery/rest?version=v1
- **API base URL:** `https://forms.googleapis.com/v1/forms`

## Authentication

### OAuth 2.0

The use of raw or derived user data received from Workspace APIs will adhere to the Google User Data Policy, including the Limited Use requirements.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.google.com/o/oauth2/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.googleapis.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `https://www.googleapis.com/auth/forms.body https://www.googleapis.com/auth/forms.responses.readonly https://www.googleapis.com/auth/drive.file openid https://www.googleapis.com/auth/userinfo.email https://www.googleapis.com/auth/userinfo.profile`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://oauth2.googleapis.com/token.

[Official authentication documentation](https://developers.google.com/workspace/forms/api/guides/authorizing)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `pageSize` in the query string to set the page size (default 20; accepted range 1–5000). Use `pageToken` in the query string as the pagination cursor.

## Sorting

Set the sort field with `orderBy` in the query string. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Questions To Form](actions/add-questions-to-form.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
| [Batch Update Form](actions/batch-update-form.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
| [Create Choice Question](actions/create-choice-question.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
| [Create Date Question](actions/create-date-question.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
| [Create Form](actions/create-form.md) | `POST /` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/create) |
| [Create Form Watch](actions/create-form-watch.md) | `POST /:formId/watches` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms.watches/create) |
| [Create Image Item](actions/create-image-item.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
| [Create Question Group Item](actions/create-question-group-item.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
| [Create Question Item](actions/create-question-item.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
| [Create Rating Question](actions/create-rating-question.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
| [Create Scale Question](actions/create-scale-question.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
| [Create Section Header Item](actions/create-section-header-item.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
| [Create Text Item](actions/create-text-item.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
| [Create Text Question](actions/create-text-question.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
| [Create Time Question](actions/create-time-question.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
| [Create Video Item](actions/create-video-item.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
| [Delete Form Item](actions/delete-form-item.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
| [Delete Form Watch](actions/delete-form-watch.md) | `DELETE /:formId/watches/:watchId` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms.watches/delete) |
| [Get Form](actions/get-form.md) | `GET /:formId` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/get) |
| [Get Form Response](actions/get-form-response.md) | `GET /:formId/responses/:responseId` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms.responses/get) |
| [List Form Responses](actions/list-form-responses.md) | `GET /:formId/responses` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms.responses/list) |
| [List Form Watches](actions/list-form-watches.md) | `GET /:formId/watches` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms.watches/list) |
| [Move Form Item](actions/move-form-item.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
| [Move Question To Section](actions/move-question-to-section.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
| [Renew Form Watch](actions/renew-form-watch.md) | `POST /:formId/watches/:watchId:renew` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms.watches/renew) |
| [Set Collect Email](actions/set-collect-email.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
| [Set Publish Settings](actions/set-publish-settings.md) | `POST /:formId:setPublishSettings` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/setPublishSettings) |
| [Set Quiz Mode](actions/set-quiz-mode.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
| [Update Form Info](actions/update-form-info.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
| [Update Form Item](actions/update-form-item.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
| [Update Form Settings](actions/update-form-settings.md) | `POST /:formId:batchUpdate` | [docs](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate) |
