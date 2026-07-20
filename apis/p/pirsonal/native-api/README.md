# Pirsonal: Native API Reference

A consolidated summary of Pirsonal's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://app.pirsonal.com/docAPI
- **API base URL:** `https://app.pirsonal.com`

## Authentication

### Account credentials

Connect Pirsonal with the account ID and account secret used as query parameters on API requests.

### Credentials

- **Account ID:** `accountID` · required · Pirsonal account identifier used in the accountID query parameter.
- **Account Secret:** `accountSecret` · required · Pirsonal secret token used in the accountSecret query parameter.

[Official authentication documentation](https://app.pirsonal.com/docAPI)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `result`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Apply Media Pattern](actions/apply-media-pattern.md) | `POST /api` | [docs](https://app.pirsonal.com/docAPI#Media_Apply_Pattern) |
| [Create Template](actions/create-template.md) | `POST /api` | [docs](https://app.pirsonal.com/docAPI#Template_New) |
| [Create Video From Template](actions/create-video-from-template.md) | `POST /api` | [docs](https://app.pirsonal.com/docAPI#Template_Video_New) |
| [Delete Media](actions/delete-media.md) | `POST /api` | [docs](https://app.pirsonal.com/docAPI#Media_Delete) |
| [Delete Template](actions/delete-template.md) | `POST /api` | [docs](https://app.pirsonal.com/docAPI#Template_Delete) |
| [Delete Video](actions/delete-video.md) | `POST /api` | [docs](https://app.pirsonal.com/docAPI#Video_Delete) |
| [Get Pirsonal Video Link](actions/get-pirsonal-video-link.md) | `POST /api` | [docs](https://app.pirsonal.com/docAPI#Video_Pirsonal_Link) |
| [Get Video](actions/get-video.md) | `POST /api` | [docs](https://app.pirsonal.com/docAPI#Video_Get) |
| [List Media](actions/list-media.md) | `POST /api` | [docs](https://app.pirsonal.com/docAPI#Media_List) |
| [List Template Videos](actions/list-template-videos.md) | `POST /api` | [docs](https://app.pirsonal.com/docAPI#Template_Video_List) |
| [List Templates](actions/list-templates.md) | `POST /api` | [docs](https://app.pirsonal.com/docAPI#Template_List) |
| [List Video Links](actions/list-video-links.md) | `POST /api` | [docs](https://app.pirsonal.com/docAPI#Video_Get_Links) |
| [Set Template Status](actions/set-template-status.md) | `POST /api` | [docs](https://app.pirsonal.com/docAPI#Template_SetStatus) |
| [Update Template](actions/update-template.md) | `POST /api` | [docs](https://app.pirsonal.com/docAPI#Template_Update) |
| [Update Video](actions/update-video.md) | `POST /api` | [docs](https://app.pirsonal.com/docAPI#Video_Update) |
| [Update Video Metadata](actions/update-video-metadata.md) | `POST /api` | [docs](https://app.pirsonal.com/docAPI#Video_Update_Metadata) |
