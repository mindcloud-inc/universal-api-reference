# Typeform: Native API Reference

A consolidated summary of Typeform's API configuration and 48 documented operations, with links to official documentation.

- **Official docs:** https://www.typeform.com/developers/
- **API base URL:** `https://api.typeform.com`

## Authentication

### Personal Access Token

Use a Typeform personal access token. MindCloud sends it as Authorization: Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.typeform.com/hc/en-us/articles/13599952215572-Typeform-API-personal-access-token)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 10; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `order_by`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (48 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Auto-Translate Form](actions/auto-translate-form.md) | `POST /forms/:formId/translations/:language/auto` | [docs](https://www.typeform.com/developers/create/reference/auto-translate-form/) |
| [Create Account Workspace](actions/create-account-workspace.md) | `POST /accounts/:accountId/workspaces` | [docs](https://www.typeform.com/developers/create/reference/create-account-workspace/) |
| [Create Form](actions/create-form.md) | `POST /forms` | [docs](https://www.typeform.com/developers/create/reference/create-form/) |
| [Create Image](actions/create-image.md) | `POST /images` | [docs](https://www.typeform.com/developers/create/reference/create-image/) |
| [Create or Update Webhook](actions/create-or-update-webhook.md) | `PUT /forms/:formId/webhooks/:tag` | [docs](https://www.typeform.com/developers/webhooks/reference/create-or-update-webhook/) |
| [Create Theme](actions/create-theme.md) | `POST /themes` | [docs](https://www.typeform.com/developers/create/reference/create-theme/) |
| [Create Workspace](actions/create-workspace.md) | `POST /workspaces` | [docs](https://www.typeform.com/developers/create/reference/create-workspace/) |
| [Delete Form](actions/delete-form.md) | `DELETE /forms/:formId` | [docs](https://www.typeform.com/developers/create/reference/delete-form/) |
| [Delete Form Translation](actions/delete-form-translation.md) | `DELETE /forms/:formId/translations/:language` | [docs](https://www.typeform.com/developers/create/reference/delete-form-translation/) |
| [Delete Image](actions/delete-image.md) | `DELETE /images/:imageId` | [docs](https://www.typeform.com/developers/create/reference/delete-image/) |
| [Delete Responses](actions/delete-responses.md) | `DELETE /forms/:formId/responses` | [docs](https://www.typeform.com/developers/responses/reference/delete-responses/) |
| [Delete Theme](actions/delete-theme.md) | `DELETE /themes/:themeId` | [docs](https://www.typeform.com/developers/create/reference/delete-theme/) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /forms/:formId/webhooks/:tag` | [docs](https://www.typeform.com/developers/webhooks/reference/delete-webhook/) |
| [Delete Workspace](actions/delete-workspace.md) | `DELETE /workspaces/:workspaceId` | [docs](https://www.typeform.com/developers/create/reference/delete-workspace/) |
| [Download All Files Uploaded by Respondents for a Form](actions/download-all-files-uploaded-by-respondents-for-a-form.md) | `GET /forms/:formId/responses/files` | [docs](https://www.typeform.com/developers/responses/reference/download-all-files-uploaded-by-respondents-for-a-form/) |
| [Get a File from a Response](actions/get-a-file-from-a-response.md) | `GET /forms/:formId/responses/:responseId/fields/:fieldId/files/:filename` | [docs](https://www.typeform.com/developers/responses/reference/get-a-file-from-a-response/) |
| [Get Audio Master File (Download)](actions/get-audio-master-file-download.md) | `GET /media/audios/:id/master` | [docs](https://www.typeform.com/developers/responses/reference/get-audio-master-file-download/) |
| [Get Current User Details](actions/get-current-user-details.md) | `GET /me` | [docs](https://www.typeform.com/developers/get-started/#hands-on) |
| [Get Form](actions/get-form.md) | `GET /forms/:formId` | [docs](https://www.typeform.com/developers/create/reference/retrieve-form/) |
| [Get Video Master File (Download)](actions/get-video-master-file-download.md) | `GET /media/videos/:id/master` | [docs](https://www.typeform.com/developers/responses/reference/get-video-master-file-download/) |
| [List Account Workspaces](actions/list-account-workspaces.md) | `GET /accounts/:accountId/workspaces` | [docs](https://www.typeform.com/developers/create/reference/retrieve-account-workspaces/) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://www.typeform.com/developers/create/reference/retrieve-forms/) |
| [List Images](actions/list-images.md) | `GET /images` | [docs](https://www.typeform.com/developers/create/reference/retrieve-images-collection/) |
| [List Responses](actions/list-responses.md) | `GET /forms/:formId/responses` | [docs](https://www.typeform.com/developers/responses/reference/retrieve-responses/) |
| [List Themes](actions/list-themes.md) | `GET /themes` | [docs](https://www.typeform.com/developers/create/reference/retrieve-themes/) |
| [List Translation Statuses](actions/list-translation-statuses.md) | `GET /forms/:formId/translations/status` | [docs](https://www.typeform.com/developers/create/reference/retrieve-translation-statuses/) |
| [List Webhooks](actions/list-webhooks.md) | `GET /forms/:formId/webhooks` | [docs](https://www.typeform.com/developers/webhooks/reference/retrieve-webhooks/) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://www.typeform.com/developers/create/reference/retrieve-workspaces/) |
| [Request Audio Master File Generation](actions/request-audio-master-file-generation.md) | `POST /media/audios/:id/master` | [docs](https://www.typeform.com/developers/responses/reference/request-audio-master-file-generation/) |
| [Request Video Master File Generation](actions/request-video-master-file-generation.md) | `POST /media/videos/:id/master` | [docs](https://www.typeform.com/developers/responses/reference/request-video-master-file-generation/) |
| [Retrieve Background by Size](actions/retrieve-background-by-size.md) | `GET /images/:imageId/background/:size` | [docs](https://www.typeform.com/developers/create/reference/retrieve-background-by-size/) |
| [Retrieve Choice Image by Size](actions/retrieve-choice-image-by-size.md) | `GET /images/:imageId/choice/:size` | [docs](https://www.typeform.com/developers/create/reference/retrieve-choice-image-by-size/) |
| [Retrieve Custom Form Messages](actions/retrieve-custom-form-messages.md) | `GET /forms/:formId/messages` | [docs](https://www.typeform.com/developers/create/reference/retrieve-custom-form-messages/) |
| [Retrieve Form Translation](actions/retrieve-form-translation.md) | `GET /forms/:formId/translations/:language` | [docs](https://www.typeform.com/developers/create/reference/retrieve-form-translation/) |
| [Retrieve Image](actions/retrieve-image.md) | `GET /images/:imageId` | [docs](https://www.typeform.com/developers/create/reference/retrieve-image/) |
| [Retrieve Image by Size](actions/retrieve-image-by-size.md) | `GET /images/:imageId/image/:size` | [docs](https://www.typeform.com/developers/create/reference/retrieve-image-by-size/) |
| [Retrieve Single Webhook](actions/retrieve-single-webhook.md) | `GET /forms/:formId/webhooks/:tag` | [docs](https://www.typeform.com/developers/webhooks/reference/retrieve-single-webhook/) |
| [Retrieve Theme](actions/retrieve-theme.md) | `GET /themes/:themeId` | [docs](https://www.typeform.com/developers/create/reference/retrieve-theme/) |
| [Retrieve Translation Payload](actions/retrieve-translation-payload.md) | `GET /forms/:formId/translations/main` | [docs](https://www.typeform.com/developers/create/reference/retrieve-translation-payload/) |
| [Retrieve Workspace](actions/retrieve-workspace.md) | `GET /workspaces/:workspaceId` | [docs](https://www.typeform.com/developers/create/reference/retrieve-workspace/) |
| [Update Custom Messages](actions/update-custom-messages.md) | `PUT /forms/:formId/messages` | [docs](https://www.typeform.com/developers/create/reference/update-custom-messages/) |
| [Update Form](actions/update-form.md) | `PUT /forms/:formId` | [docs](https://www.typeform.com/developers/create/reference/update-form/) |
| [Update Form (Patch)](actions/update-form-patch.md) | `PATCH /forms/:formId` | [docs](https://www.typeform.com/developers/create/reference/update-form-patch/) |
| [Update Form Translation](actions/update-form-translation.md) | `PUT /forms/:formId/translations/:language` | [docs](https://www.typeform.com/developers/create/reference/update-form-translation/) |
| [Update Theme (Partial Update)](actions/update-theme-partial-update.md) | `PATCH /themes/:themeId` | [docs](https://www.typeform.com/developers/create/reference/update-theme-partial-update/) |
| [Update Theme (Whole Definition)](actions/update-theme-whole-definition.md) | `PUT /themes/:themeId` | [docs](https://www.typeform.com/developers/create/reference/update-theme-whole-definition/) |
| [Update Workspace](actions/update-workspace.md) | `PATCH /workspaces/:workspaceId` | [docs](https://www.typeform.com/developers/create/reference/update-workspace/) |
| [Upload a Video File](actions/upload-a-video-file.md) | `POST /media/videos` | [docs](https://www.typeform.com/developers/create/reference/upload-a-video-file/) |
