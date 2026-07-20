# Dropbox: Native API Reference

A consolidated summary of Dropbox's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://www.dropbox.com/developers/documentation/http/documentation
- **API base URL:** `https://api.dropboxapi.com/2`

## Authentication

### OAuth 2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.dropbox.com/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.dropboxapi.com/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `account_info.write account_info.read files.metadata.write files.metadata.read files.content.write files.content.read sharing.write sharing.read file_requests.write file_requests.read contacts.write contacts.read team_info.write team_info.read team_data.member team_data.team_space team_data.governance.write team_data.governance.read team_data.content.write team_data.content.read files.team_metadata.write files.team_metadata.read files.permanent_delete members.write members.read members.delete groups.write groups.read sessions.modify sessions.list events.write events.read`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.dropboxapi.com/oauth2/token.

[Official authentication documentation](https://developers.dropbox.com/oauth-guide)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add File Members](actions/add-file-members.md) | `POST /sharing/add_file_member` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#sharing-add_file_member) |
| [Add Shared Folder Members](actions/add-shared-folder-members.md) | `POST /sharing/add_folder_member` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#sharing-add_folder_member) |
| [Continue Folder Listing](actions/continue-folder-listing.md) | `POST /files/list_folder/continue` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#files-list_folder/continue) |
| [Copy File or Folder](actions/copy-file-or-folder.md) | `POST /files/copy_v2` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#files-copy_v2) |
| [Create File Request](actions/create-file-request.md) | `POST /file_requests/create` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#file_requests-create) |
| [Create Folder](actions/create-folder.md) | `POST /files/create_folder_v2` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#files-create_folder_v2) |
| [Create Shared Link](actions/create-shared-link.md) | `POST /sharing/create_shared_link_with_settings` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#sharing-create_shared_link_with_settings) |
| [Delete File or Folder](actions/delete-file-or-folder.md) | `POST /files/delete_v2` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#files-delete_v2) |
| [Download File](actions/download-file.md) | `POST https://content.dropboxapi.com/2/files/download` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#files-download) |
| [Get Account](actions/get-account.md) | `POST /users/get_account` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#users-get_account) |
| [Get Current Account](actions/get-current-account.md) | `POST /users/get_current_account` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#users-get_current_account) |
| [Get File or Folder Metadata](actions/get-file-or-folder-metadata.md) | `POST /files/get_metadata` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#files-get_metadata) |
| [Get File Request](actions/get-file-request.md) | `POST /file_requests/get` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#file_requests-get) |
| [Get Latest Folder Cursor](actions/get-latest-folder-cursor.md) | `POST /files/list_folder/get_latest_cursor` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#files-list_folder/get_latest_cursor) |
| [Get Shared Link Metadata](actions/get-shared-link-metadata.md) | `POST /sharing/get_shared_link_metadata` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#sharing-get_shared_link_metadata) |
| [Get Space Usage](actions/get-space-usage.md) | `POST /users/get_space_usage` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#users-get_space_usage) |
| [Get Temporary Link](actions/get-temporary-link.md) | `POST /files/get_temporary_link` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#files-get_temporary_link) |
| [List File Requests](actions/list-file-requests.md) | `POST /file_requests/list_v2` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#file_requests-list_v2) |
| [List File Revisions](actions/list-file-revisions.md) | `POST /files/list_revisions` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#files-list_revisions) |
| [List Folder Contents](actions/list-folder-contents.md) | `POST /files/list_folder` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#files-list_folder) |
| [List Shared Folder Members](actions/list-shared-folder-members.md) | `POST /sharing/list_folder_members` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#sharing-list_folder_members) |
| [List Shared Folders](actions/list-shared-folders.md) | `POST /sharing/list_folders` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#sharing-list_folders) |
| [List Shared Links](actions/list-shared-links.md) | `POST /sharing/list_shared_links` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#sharing-list_shared_links) |
| [Move File or Folder](actions/move-file-or-folder.md) | `POST /files/move_v2` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#files-move_v2) |
| [Restore File Revision](actions/restore-file-revision.md) | `POST /files/restore` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#files-restore) |
| [Revoke Shared Link](actions/revoke-shared-link.md) | `POST /sharing/revoke_shared_link` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#sharing-revoke_shared_link) |
| [Search Files and Folders](actions/search-files-and-folders.md) | `POST /files/search_v2` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#files-search_v2) |
| [Update File Request](actions/update-file-request.md) | `POST /file_requests/update` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#file_requests-update) |
| [Update Shared Link Settings](actions/update-shared-link-settings.md) | `POST /sharing/modify_shared_link_settings` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#sharing-modify_shared_link_settings) |
| [Upload File](actions/upload-file.md) | `POST https://content.dropboxapi.com/2/files/upload` | [docs](https://www.dropbox.com/developers/documentation/http/documentation#files-upload) |
