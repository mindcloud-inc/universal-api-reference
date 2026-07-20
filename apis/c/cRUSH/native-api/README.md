# CRUSH: Native API Reference

A consolidated summary of CRUSH's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://app.crushthememory.com/dashboard
- **API base URL:** `https://app.crushthememory.com/api`

## Authentication

### API Key

Use a CRUSH API key generated from Dashboard -> AP -> API Key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.crushthememory.com/dashboard)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Audio Download URL](actions/get-audio-download-url.md) | `GET /aws/audio` | [docs](https://app.crushthememory.com/dashboard) |
| [Get Note](actions/get-note.md) | `GET /aws/noteflags` | [docs](https://app.crushthememory.com/dashboard) |
| [Get User Profile](actions/get-user-profile.md) | `GET /aws/userprofiles` | [docs](https://app.crushthememory.com/dashboard) |
| [List API Tokens](actions/list-api-tokens.md) | `GET /tokens` | [docs](https://app.crushthememory.com/dashboard) |
| [List Folder Metadata](actions/list-folder-metadata.md) | `GET /aws/insights` | [docs](https://app.crushthememory.com/dashboard) |
| [List Folders](actions/list-folders.md) | `GET /aws/noteflags` | [docs](https://app.crushthememory.com/dashboard) |
| [List Notes](actions/list-notes.md) | `GET /aws/noteflags` | [docs](https://app.crushthememory.com/dashboard) |
| [List Tags](actions/list-tags.md) | `GET /aws/tags` | [docs](https://app.crushthememory.com/dashboard) |
