# Box: Native API Reference

A consolidated summary of Box's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://developer.box.com/reference
- **API base URL:** `https://api.box.com/2.0`

## Authentication

### OAuth 2.0

Connect a Box user account through the standard OAuth 2.0 authorization-code flow.

### Credentials

- **Client Id:** `clientId` · required
- **Client Secret:** `clientSecret` · required

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://account.box.com/api/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.box.com/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `root_readwrite`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.box.com/oauth2/token.

[Official authentication documentation](https://developer.box.com/guides/authentication/oauth2/oauth2-setup)

### Developer Token

Expires Quickly

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.box.com/guides/authentication/oauth2/oauth2-setup)

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Commit Upload Session](actions/commit-upload-session.md) | `POST https://upload.box.com/api/2.0/files/upload_sessions/:session_id/commit` | [docs](https://developer.box.com/reference/post-files-upload-sessions-id-commit) |
| [Create Folder](actions/create-folder.md) | `POST /folders` | [docs](https://developer.box.com/reference/post-folders) |
| [Create Upload Session](actions/create-upload-session.md) | `POST https://upload.box.com/api/2.0/files/upload_sessions` | [docs](https://developer.box.com/reference/post-files-upload-sessions) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://developer.box.com/reference/get-users-me) |
| [Get Folder](actions/get-folder.md) | `GET /folders/:folder_id` | [docs](https://developer.box.com/reference/get-folders-id) |
| [List Root Folder Items](actions/list-root-folder-items.md) | `GET /folders/:folder_id/items` | [docs](https://developer.box.com/reference/get-folders-id-items) |
| [Search Folders](actions/search-folders.md) | `GET /search` | [docs](https://developer.box.com/reference/get-search) |
| [Upload Part](actions/upload-part.md) | `PUT https://upload.box.com/api/2.0/files/upload_sessions/:session_id` | [docs](https://developer.box.com/reference/put-files-upload-sessions-id) |
