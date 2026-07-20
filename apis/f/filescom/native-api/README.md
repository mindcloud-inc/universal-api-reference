# Files.com: Native API Reference

A consolidated summary of Files.com's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://www.files.com/docs/sdk-and-apis
- **API base URL:** `{siteUrl}/api/rest/v1`

## Authentication

### Files.com Header API Key

Authenticate with a Files.com API key sent only in the X-FilesAPI-Key header. Files.com API keys inherit the owning user's permissions.

### Credentials

- **Site URL:** `siteUrl` · required · Full Files.com site URL, for example https://your-subdomain.files.com. Do not include /api/rest/v1.
- **API Key:** `apiKey` · required · Files.com API key to send in the X-FilesAPI-Key header. This key inherits the owning user's permissions; admin actions need a site-admin service user.

Send these headers with each API request:

```http
X-FilesAPI-Key: <apiKey>
```

[Official authentication documentation](https://developers.files.com/rest/overview/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (accepted range 1–10000). Use `cursor` in the query string as the pagination cursor; numbering starts at 0.

## Endpoints (38 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Begin File Upload](actions/begin-file-upload.md) | `POST /file_actions/begin_upload/:path` | [docs](https://developers.files.com/rest/files/files#upload-file-optimized) |
| [Copy File or Folder](actions/copy-file-or-folder.md) | `POST /file_actions/copy/:path` | [docs](https://developers.files.com/rest/files/files#copy-filefolder) |
| [Create Folder](actions/create-folder.md) | `POST /folders/:path` | [docs](https://developers.files.com/rest/files/files#create-folder) |
| [Delete File or Folder](actions/delete-file-or-folder.md) | `DELETE /files/:path` | [docs](https://developers.files.com/rest/files/files#delete-filefolder) |
| [Get Automation](actions/get-automation.md) | `GET /automations/:id` | [docs](https://developers.files.com/rest/resources/automations/automations#show-automation) |
| [Get Bundle](actions/get-bundle.md) | `GET /bundles/:id` | [docs](https://developers.files.com/rest/resources/sharing/share-links/bundles#show-share-link) |
| [Get File Download Link](actions/get-file-download-link.md) | `GET /files/:path` | [docs](https://developers.files.com/rest/files/files#download-file-optimized) |
| [Get File or Folder Metadata](actions/get-file-or-folder-metadata.md) | `GET /file_actions/metadata/:path` | [docs](https://developers.files.com/rest/files/files#find-filefolder-by-path) |
| [Get Group](actions/get-group.md) | `GET /groups/:id` | [docs](https://developers.files.com/rest/resources/user-accounts/groups#show-group) |
| [Get Notification](actions/get-notification.md) | `GET /notifications/:id` | [docs](https://developers.files.com/rest/resources/notifications/notifications/#show-notification) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://developers.files.com/rest/resources/file-system/project-management/projects#show-project) |
| [Get Site](actions/get-site.md) | `GET /site` | [docs](https://developers.files.com/rest/resources/settings/sites#show-site-settings) |
| [Get Site Usage](actions/get-site-usage.md) | `GET /site/usage` | [docs](https://www.files.com/docs/logging/site-usage) |
| [Get Sync](actions/get-sync.md) | `GET /syncs/:id` | [docs](https://developers.files.com/rest/resources/integrations/syncs#show-sync) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://developers.files.com/rest/resources/user-accounts/users#show-user) |
| [Get Workspace](actions/get-workspace.md) | `GET /workspaces/:id` | [docs](https://developers.files.com/rest/resources/user-accounts/workspaces#show-workspace) |
| [List Automations](actions/list-automations.md) | `GET /automations` | [docs](https://developers.files.com/rest/resources/automations/automations#list-automations) |
| [List Bundles](actions/list-bundles.md) | `GET /bundles` | [docs](https://developers.files.com/rest/resources/sharing/share-links/bundles#list-share-links) |
| [List File Comments](actions/list-file-comments.md) | `GET /file_comments/files/:path` | [docs](https://developers.files.com/rest/resources/file-system/file-comments#list-file-comments-by-path) |
| [List File History](actions/list-file-history.md) | `GET /history/files/:path` | [docs](https://developers.files.com/rest/resources/logging/actions#list-history-for-specific-file) |
| [List Folder Contents](actions/list-folder-contents.md) | `GET /folders/:path` | [docs](https://developers.files.com/rest/files/files#list-folders-by-path) |
| [List Folder History](actions/list-folder-history.md) | `GET /history/folders/:path` | [docs](https://developers.files.com/rest/resources/logging/actions/#list-history-for-specific-folder) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://developers.files.com/rest/resources/user-accounts/groups#list-groups) |
| [List History](actions/list-history.md) | `GET /history` | [docs](https://developers.files.com/rest/resources/logging/actions#list-site-full-action-history) |
| [List Login History](actions/list-login-history.md) | `GET /history/login` | [docs](https://developers.files.com/rest/resources/logging/actions/#list-site-login-history) |
| [List Notifications](actions/list-notifications.md) | `GET /notifications` | [docs](https://developers.files.com/rest/resources/notifications/notifications/#list-notifications) |
| [List Permissions](actions/list-permissions.md) | `GET /permissions` | [docs](https://developers.files.com/rest/resources/user-accounts/permissions#list-permissions) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://developers.files.com/rest/resources/file-system/project-management/projects#list-projects) |
| [List Requests](actions/list-requests.md) | `GET /requests` | [docs](https://developers.files.com/rest/resources/file-system/requests/#list-requests) |
| [List Requests by Folder Path](actions/list-requests-by-folder-path.md) | `GET /requests/folders/:path` | [docs](https://developers.files.com/rest/resources/file-system/requests/#list-requests) |
| [List Syncs](actions/list-syncs.md) | `GET /syncs` | [docs](https://developers.files.com/rest/resources/integrations/syncs#list-syncs) |
| [List User History](actions/list-user-history.md) | `GET /history/users/:user_id` | [docs](https://developers.files.com/rest/resources/logging/actions/#list-history-for-specific-user) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developers.files.com/rest/resources/user-accounts/users#list-users) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://developers.files.com/rest/resources/user-accounts/workspaces#list-workspaces) |
| [Move File or Folder](actions/move-file-or-folder.md) | `POST /file_actions/move/:path` | [docs](https://developers.files.com/rest/files/files#move-filefolder) |
| [Run Automation Now](actions/run-automation-now.md) | `POST /automations/:id/manual_run` | [docs](https://developers.files.com/rest/resources/automations/automations#manually-run-automation) |
| [Run Sync Now](actions/run-sync-now.md) | `POST /syncs/:id/manual_run` | [docs](https://developers.files.com/rest/resources/integrations/syncs#manually-run-sync) |
| [Update File or Folder Metadata](actions/update-file-or-folder-metadata.md) | `PATCH /files/:path` | [docs](https://developers.files.com/rest/files/files#update-filefolder-metadata) |
