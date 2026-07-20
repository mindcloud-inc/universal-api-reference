# HackMD: Native API Reference

A consolidated summary of HackMD's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://api.hackmd.io/v1/docs
- **OpenAPI specification:** https://api.hackmd.io/v1/docs/swagger.json
- **API base URL:** `https://api.hackmd.io/v1`

## Authentication

### API Key

Bearer token authentication for the HackMD API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://hackmd.io/%40hackmd-api/api-authorization)

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | `POST /notes` | [docs](https://api.hackmd.io/v1/docs) |
| [Delete Note](actions/delete-note.md) | `DELETE /notes/:noteId` | [docs](https://api.hackmd.io/v1/docs) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://api.hackmd.io/v1/docs) |
| [Get Note](actions/get-note.md) | `GET /notes/:noteId` | [docs](https://api.hackmd.io/v1/docs) |
| [List Note History](actions/list-note-history.md) | `GET /history` | [docs](https://api.hackmd.io/v1/docs) |
| [List Notes](actions/list-notes.md) | `GET /notes` | [docs](https://api.hackmd.io/v1/docs) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://api.hackmd.io/v1/docs) |
| [Update Note](actions/update-note.md) | `PATCH /notes/:noteId` | [docs](https://api.hackmd.io/v1/docs) |
