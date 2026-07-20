# Wistia: Native API Reference

A consolidated summary of Wistia's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.wistia.com/reference
- **API base URL:** `https://api.wistia.com`

## Authentication

### API Key

Use a Wistia API token as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.wistia.com/reference/getting-started-with-the-upload-api-1)

## API conventions

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Media](actions/archive-media.md) | `PUT /modern/medias/archive` | [docs](https://docs.wistia.com/reference/put_medias-archive) |
| [Create Captions](actions/create-captions.md) | `POST /modern/medias/:mediaHashedId/captions` | [docs](https://docs.wistia.com/reference/post_medias-mediahashedid-captions) |
| [Create Folder](actions/create-folder.md) | `POST /v1/projects` | [docs](https://docs.wistia.com/reference/post_projects) |
| [Create Subfolder](actions/create-subfolder.md) | `POST /v1/projects/:projectId/subfolders` | [docs](https://docs.wistia.com/reference/post_projects-projectid-subfolders) |
| [Delete Captions](actions/delete-captions.md) | `DELETE /modern/medias/:mediaHashedId/captions/:languageCode` | [docs](https://docs.wistia.com/reference/delete_medias-mediahashedid-captions-languagecode) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /v1/projects/:id` | [docs](https://docs.wistia.com/reference/delete_projects-id) |
| [Delete Media](actions/delete-media.md) | `DELETE /modern/medias/:mediaHashedId` | [docs](https://docs.wistia.com/reference/delete_medias-mediahashedid) |
| [Delete Subfolder](actions/delete-subfolder.md) | `DELETE /v1/projects/:projectId/subfolders/:subfolderId` | [docs](https://docs.wistia.com/reference/delete_projects-projectid-subfolders-subfolderid) |
| [Get Current Account](actions/get-current-account.md) | `GET /modern/account` | [docs](https://docs.wistia.com/reference/getaccountdetails) |
| [Get Folder](actions/get-folder.md) | `GET /v1/projects/:id` | [docs](https://docs.wistia.com/reference/get_projects-id) |
| [Get Media Aggregated Stats](actions/get-media-aggregated-stats.md) | `GET /stats/medias/:mediaHashedId.json` | [docs](https://docs.wistia.com/reference/get_media_stats) |
| [List Captions by Media](actions/list-captions-by-media.md) | `GET /modern/medias/:mediaHashedId/captions` | [docs](https://docs.wistia.com/reference/get_medias-mediahashedid-captions) |
| [List Folders](actions/list-folders.md) | `GET /v1/projects` | [docs](https://docs.wistia.com/reference/get_projects) |
| [List Media](actions/list-media.md) | `GET /modern/medias` | [docs](https://docs.wistia.com/reference/get_medias) |
| [List Subfolders](actions/list-subfolders.md) | `GET /v1/projects/:projectId/subfolders` | [docs](https://docs.wistia.com/reference/get_projects-projectid-subfolders) |
| [Move Media](actions/move-media.md) | `PUT /modern/medias/move` | [docs](https://docs.wistia.com/reference/put_medias-move) |
| [Restore Media](actions/restore-media.md) | `PUT /modern/medias/restore` | [docs](https://docs.wistia.com/reference/put_medias-restore) |
| [Search Wistia](actions/search-wistia.md) | `GET /modern/search` | [docs](https://docs.wistia.com/reference/get_search) |
| [Show Background Job Status](actions/show-background-job-status.md) | `GET /modern/background_job_status/:backgroundJobStatusId` | [docs](https://docs.wistia.com/reference/get_background-job-status-backgroundjobstatusid) |
| [Show Captions](actions/show-captions.md) | `GET /modern/medias/:mediaHashedId/captions/:languageCode` | [docs](https://docs.wistia.com/reference/get_medias-mediahashedid-captions-languagecode) |
| [Show Customizations](actions/show-customizations.md) | `GET /modern/medias/:mediaId/customizations` | [docs](https://docs.wistia.com/reference/get_medias-mediaid-customizations) |
| [Show Media](actions/show-media.md) | `GET /modern/medias/:mediaHashedId` | [docs](https://docs.wistia.com/reference/get_medias-mediahashedid) |
| [Swap Media](actions/swap-media.md) | `PUT /modern/medias/:mediaHashedId/swap` | [docs](https://docs.wistia.com/reference/put_medias-mediahashedid-swap) |
| [Translate Media](actions/translate-media.md) | `POST /modern/medias/:mediaHashedId/translate` | [docs](https://docs.wistia.com/reference/post_medias-mediahashedid-translate) |
| [Update Captions](actions/update-captions.md) | `PUT /modern/medias/:mediaHashedId/captions/:languageCode` | [docs](https://docs.wistia.com/reference/put_medias-mediahashedid-captions-languagecode) |
| [Update Customizations](actions/update-customizations.md) | `PUT /modern/medias/:mediaId/customizations` | [docs](https://docs.wistia.com/reference/put_medias-mediaid-customizations) |
| [Update Folder](actions/update-folder.md) | `PUT /v1/projects/:id` | [docs](https://docs.wistia.com/reference/put_projects-id) |
| [Update Media](actions/update-media.md) | `PUT /modern/medias/:mediaHashedId` | [docs](https://docs.wistia.com/reference/put_medias-mediahashedid) |
| [Update Subfolder](actions/update-subfolder.md) | `PUT /v1/projects/:projectId/subfolders/:subfolderId` | [docs](https://docs.wistia.com/reference/put_projects-projectid-subfolders-subfolderid) |
| [Upload Or Import Media](actions/upload-or-import-media.md) | `POST https://upload.wistia.com/` | [docs](https://docs.wistia.com/reference/post_) |
