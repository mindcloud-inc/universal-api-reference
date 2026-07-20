# Seafile: Native API Reference

A consolidated summary of Seafile's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://seafile-api.readme.io/reference/introduction
- **API base URL:** `https://plus.seafile.com/api2`

## Authentication

### Account Token

Authenticate Seafile API requests with an account token.

### Credentials

- **Account Token:** `accountToken` · required · Seafile account token used in the Authorization header.

[Official authentication documentation](https://seafile-api.readme.io/reference/account-token)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | `GET https://plus.seafile.com/api2/account/info/` | [docs](https://seafile-api.readme.io/reference/get_api2-account-info) |
| [Get Default Library](actions/get-default-library.md) | `GET https://plus.seafile.com/api2/default-repo/` | [docs](https://seafile-api.readme.io/reference/get_api2-default-repo) |
| [Get Directory Detail](actions/get-directory-detail.md) | `GET https://plus.seafile.com/api/v2.1/repos/{repoId}/dir/detail/` | [docs](https://seafile-api.readme.io/reference/get_api-v2-1-repos-repo-id-dir-detail) |
| [Get File Activities](actions/get-file-activities.md) | `GET https://plus.seafile.com/api/v2.1/activities/` | [docs](https://seafile-api.readme.io/reference/get_api-v2-1-activities) |
| [Get File Detail](actions/get-file-detail.md) | `GET https://plus.seafile.com/api2/repos/{repoId}/file/detail/` | [docs](https://seafile-api.readme.io/reference/get_api2-repos-repo-id-file-detail) |
| [Get File History](actions/get-file-history.md) | `GET https://plus.seafile.com/api/v2.1/repos/{repoId}/file/history/` | [docs](https://seafile-api.readme.io/reference/get_api-v2-1-repos-repo-id-file-history) |
| [Get Group Info](actions/get-group-info.md) | `GET https://plus.seafile.com/api/v2.1/groups/{groupId}/` | [docs](https://seafile-api.readme.io/reference/get_api-v2-1-groups-group-id) |
| [Get Invitation](actions/get-invitation.md) | `GET https://plus.seafile.com/api/v2.1/invitations/{invitationToken}/` | [docs](https://seafile-api.readme.io/reference/get_api-v2-1-invitations-invitation-token) |
| [Get Library Commit Info](actions/get-library-commit-info.md) | `GET https://plus.seafile.com/api/v2.1/repos/{repoId}/commits/{commitId}/` | [docs](https://seafile-api.readme.io/reference/get_api-v2-1-repos-repo-id-commits-commit-id) |
| [Get Library History](actions/get-library-history.md) | `GET https://plus.seafile.com/api/v2.1/repos/{repoId}/history/` | [docs](https://seafile-api.readme.io/reference/get_api-v2-1-repos-repo-id-history) |
| [Get Library Info](actions/get-library-info.md) | `GET https://plus.seafile.com/api2/repos/{repo_id}/` | [docs](https://seafile-api.readme.io/reference/get_api2-repos-repo-id) |
| [Get Library Owner](actions/get-library-owner.md) | `GET https://plus.seafile.com/api2/repos/{repoId}/owner/` | [docs](https://seafile-api.readme.io/reference/get_api2-repos-repo-id-owner) |
| [Get Library Trash](actions/get-library-trash.md) | `GET https://plus.seafile.com/api/v2.1/repos/{repoId}/trash/` | [docs](https://seafile-api.readme.io/reference/get_api-v2-1-repos-repo-id-trash) |
| [Get Server Information](actions/get-server-information.md) | `GET https://plus.seafile.com/api2/server-info/` | [docs](https://seafile-api.readme.io/reference/get_api2-server-info) |
| [Get User Profile](actions/get-user-profile.md) | `GET https://plus.seafile.com/api/v2.1/user/` | [docs](https://seafile-api.readme.io/reference/get_api-v2-1-user) |
| [List All Share Links](actions/list-all-share-links.md) | `GET https://plus.seafile.com/api/v2.1/share-links/` | [docs](https://seafile-api.readme.io/reference/get_api-v2-1-share-links) |
| [List Devices](actions/list-devices.md) | `GET https://plus.seafile.com/api2/devices/` | [docs](https://seafile-api.readme.io/reference/get_api2-devices) |
| [List Folder Download Items](actions/list-folder-download-items.md) | `GET https://plus.seafile.com/api2/d/{token}/dir/` | [docs](https://seafile-api.readme.io/reference/get_api2-d-token-dir) |
| [List Folder or File Share Links](actions/list-folder-or-file-share-links.md) | `GET https://plus.seafile.com/api/v2.1/share-links/` | [docs](https://seafile-api.readme.io/reference/get_api-v2-1-share-links-repo-id-repo-id-path-path) |
| [List Group Members](actions/list-group-members.md) | `GET https://plus.seafile.com/api/v2.1/groups/{groupId}/members/` | [docs](https://seafile-api.readme.io/reference/get_api-v2-1-groups-group-id-members) |
| [List Groups](actions/list-groups.md) | `GET https://plus.seafile.com/api2/groups/` | [docs](https://seafile-api.readme.io/reference/get_api2-groups) |
| [List Invitations](actions/list-invitations.md) | `GET https://plus.seafile.com/api/v2.1/invitations/` | [docs](https://seafile-api.readme.io/reference/get_api-v2-1-invitations) |
| [List Items in Directory](actions/list-items-in-directory.md) | `GET https://plus.seafile.com/api2/repos/{repoId}/dir/` | [docs](https://seafile-api.readme.io/reference/get_api2-repos-repo-id-dir) |
| [List Libraries](actions/list-libraries.md) | `GET https://plus.seafile.com/api2/repos/` | [docs](https://seafile-api.readme.io/reference/get_api2-repos) |
| [List Libraries Shared to Me](actions/list-libraries-shared-to-me.md) | `GET https://plus.seafile.com/api2/beshared-repos/` | [docs](https://seafile-api.readme.io/reference/get_api2-beshared-repos) |
| [List Library Share Links](actions/list-library-share-links.md) | `GET https://plus.seafile.com/api/v2.1/share-links/` | [docs](https://seafile-api.readme.io/reference/get_api-v2-1-share-links-repo-id-repo-id) |
| [List Shared Library Users and Groups](actions/list-shared-library-users-and-groups.md) | `GET https://plus.seafile.com/api2/repos/{repoId}/dir/shared_items/` | [docs](https://seafile-api.readme.io/reference/get_api2-repos-repo-id-dir-shared-items) |
| [List Starred Items](actions/list-starred-items.md) | `GET https://plus.seafile.com/api/v2.1/starred-items/` | [docs](https://seafile-api.readme.io/reference/get_api-v2-1-starred-items) |
| [Search Files by Name in Library](actions/search-files-by-name-in-library.md) | `GET https://plus.seafile.com/api/v2.1/search-file/` | [docs](https://seafile-api.readme.io/reference/get_api-v2-1-search-file) |
| [Search Files in Libraries](actions/search-files-in-libraries.md) | `GET https://plus.seafile.com/api2/search/` | [docs](https://seafile-api.readme.io/reference/get_api2-search) |
