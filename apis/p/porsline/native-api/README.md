# Porsline: Native API Reference

A consolidated summary of Porsline's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://developers.porsline.com/
- **API base URL:** `https://survey.porsline.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.porsline.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `page_size` in the query string to set the page size (default 500). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Authentication Codes](actions/create-authentication-codes.md) | `POST /api/surveys/:survey_id/settings/authentication-codes/` | [docs](https://developers.porsline.com/#tag/Authentication-codes/paths/~1api~1surveys~1{survey_id}~1settings~1authentication-codes~1/post) |
| [Create Folder](actions/create-folder.md) | `POST /api/folders/` | [docs](https://developers.porsline.com/#tag/Folders/paths/~1api~1folders~1/post) |
| [Create Notification](actions/create-notification.md) | `POST /api/v2/surveys/:survey_id/notifications/` | [docs](https://developers.porsline.com/#tag/Notifications/paths/~1api~1v2~1surveys~1{survey_id}~1notifications~1/post) |
| [Create Question](actions/create-question.md) | `POST /api/v2/surveys/:survey_id/questions/` | [docs](https://developers.porsline.com/#tag/Questions/paths/~1api~1v2~1surveys~1{survey_id}~1questions~1/post) |
| [Create Variables](actions/create-variables.md) | `POST /api/surveys/:survey_id/variables/` | [docs](https://developers.porsline.com/#tag/Variables/paths/~1api~1surveys~1{survey_id}~1variables~1/post) |
| [Delete Authentication Codes](actions/delete-authentication-codes.md) | `DELETE /api/surveys/:survey_id/settings/authentication-codes/` | [docs](https://developers.porsline.com/#tag/Authentication-codes/paths/~1api~1surveys~1{survey_id}~1settings~1authentication-codes~1/delete) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /api/folders/:folder_id/` | [docs](https://developers.porsline.com/#tag/Folders/paths/~1api~1folders~1{folder_id}~1/delete) |
| [Delete Question](actions/delete-question.md) | `DELETE /api/v2/surveys/:survey_id/questions/:id/` | [docs](https://developers.porsline.com/#tag/Questions/paths/~1api~1v2~1surveys~1{survey_id}~1questions~1{id}~1/delete) |
| [Delete Survey](actions/delete-survey.md) | `DELETE /api/v2/surveys/:survey_id/` | [docs](https://developers.porsline.com/#tag/Survey/paths/~1api~1v2~1surveys~1{survey_id}~1/delete) |
| [Get Folder](actions/get-folder.md) | `GET /api/folders/:folder_id/` | [docs](https://developers.porsline.com/#tag/Folders/paths/~1api~1folders~1{folder_id}~1/get) |
| [Get Notification](actions/get-notification.md) | `GET /api/v2/surveys/:survey_id/notifications/:pk/` | [docs](https://developers.porsline.com/#tag/Notifications/paths/~1api~1v2~1surveys~1{survey_id}~1notifications~1{pk}~1/get) |
| [Get Question](actions/get-question.md) | `GET /api/v2/surveys/:survey_id/questions/:id/` | [docs](https://developers.porsline.com/#tag/Questions/paths/~1api~1v2~1surveys~1{survey_id}~1questions~1{id}~1/get) |
| [Get Survey Responses Export](actions/get-survey-responses-export.md) | `GET /api/v2/surveys/:survey_id/responses/export/` | [docs](https://developers.porsline.com/#tag/Results/paths/~1api~1v2~1surveys~1{survey_id}~1responses~1export~1/get) |
| [Get Survey Responses Results Table](actions/get-survey-responses-results-table.md) | `GET /api/v2/surveys/:survey_id/responses/results-table/` | [docs](https://developers.porsline.com/#tag/Results/paths/~1api~1v2~1surveys~1{survey_id}~1responses~1results-table~1/get) |
| [Get Survey Settings](actions/get-survey-settings.md) | `GET /api/surveys/:survey_id/settings/` | [docs](https://developers.porsline.com/#tag/Settings/paths/~1api~1surveys~1{survey_id}~1settings~1/get) |
| [Hash Hidden Fields](actions/hash-hidden-fields.md) | `POST /api/surveys/:survey_id/variables/hashes/` | [docs](https://developers.porsline.com/#tag/Hidden-Field-Encryption/paths/~1api~1surveys~1{survey_id}~1variables~1hashes~1/post) |
| [List Folders](actions/list-folders.md) | `GET /api/folders/` | [docs](https://developers.porsline.com/#tag/Folders/paths/~1api~1folders~1/get) |
| [List Notifications](actions/list-notifications.md) | `GET /api/v2/surveys/:survey_id/notifications/` | [docs](https://developers.porsline.com/#tag/Notifications/paths/~1api~1v2~1surveys~1{survey_id}~1notifications~1/get) |
| [List Survey Authentication Codes](actions/list-survey-authentication-codes.md) | `GET /api/surveys/:survey_id/settings/authentication-codes/` | [docs](https://developers.porsline.com/#tag/Authentication-codes/paths/~1api~1surveys~1{survey_id}~1settings~1authentication-codes~1/get) |
| [List Survey Variables](actions/list-survey-variables.md) | `GET /api/surveys/:survey_id/variables/` | [docs](https://developers.porsline.com/#tag/Variables/paths/~1api~1surveys~1{survey_id}~1variables~1/get) |
| [Replace Folder](actions/replace-folder.md) | `PUT /api/folders/:folder_id/` | [docs](https://developers.porsline.com/#tag/Folders/paths/~1api~1folders~1{folder_id}~1/put) |
| [Retrieve Survey](actions/retrieve-survey.md) | `GET /api/v2/surveys/:survey_id/` | [docs](https://developers.porsline.com/#tag/Survey/paths/~1api~1v2~1surveys~1{survey_id}~1/get) |
| [Update Folder](actions/update-folder.md) | `PATCH /api/folders/:folder_id/` | [docs](https://developers.porsline.com/#tag/Folders/paths/~1api~1folders~1{folder_id}~1/patch) |
| [Update Notification](actions/update-notification.md) | `PATCH /api/v2/surveys/:survey_id/notifications/:pk/` | [docs](https://developers.porsline.com/#tag/Notifications/paths/~1api~1v2~1surveys~1{survey_id}~1notifications~1{pk}~1/patch) |
| [Update Question](actions/update-question.md) | `PATCH /api/v2/surveys/:survey_id/questions/:id/` | [docs](https://developers.porsline.com/#tag/Questions/paths/~1api~1v2~1surveys~1{survey_id}~1questions~1{id}~1/patch) |
| [Update Survey Settings](actions/update-survey-settings.md) | `PATCH /api/surveys/:survey_id/settings/` | [docs](https://developers.porsline.com/#tag/Settings/paths/~1api~1surveys~1{survey_id}~1settings~1/patch) |
