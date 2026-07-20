# Histre: Native API Reference

A consolidated summary of Histre's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://histre.com/features/api/
- **API base URL:** `https://histre.com`

## Authentication

### JWT Login (Username + Password)

Use your Histre account username and password. MindCloud exchanges them for JWT access and refresh tokens through the Histre Auth API.

### Credentials

- **Username:** `username` · required · Your Histre account username used to sign in and obtain JWT tokens.
- **Password:** `password` · required · Your Histre account password used to sign in and obtain JWT tokens.

Send these headers with each API request:

```http
Authorization: Bearer <custom.access>
```

[Official authentication documentation](https://histre.com/features/api/auth/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Notes to Collections](actions/add-notes-to-collections.md) | `POST /api/v1/collections/add_notes/` | [docs](https://histre.com/features/api/collections/) |
| [Create a New Collection](actions/create-new-collection.md) | `POST /api/v1/collections/` | [docs](https://histre.com/features/api/collections/) |
| [Create Or Update Notes](actions/create-or-update-notes.md) | `POST /api/v1/note/` | [docs](https://histre.com/features/api/notes/) |
| [Delete a Collection](actions/delete-collection.md) | `DELETE /api/v1/collections/[:book_id]/` | [docs](https://histre.com/features/api/collections/) |
| [Delete Highlight](actions/delete-highlight.md) | `DELETE /api/v1/highlight/` | [docs](https://histre.com/features/api/highlights/) |
| [Delete a Note](actions/delete-note.md) | `DELETE /api/v1/note/` | [docs](https://histre.com/features/api/notes/) |
| [List All Collections](actions/list-all-collections.md) | `GET /api/v1/collections/` | [docs](https://histre.com/features/api/collections/) |
| [List Notes](actions/list-notes.md) | `GET /api/v1/note/` | [docs](https://histre.com/features/api/notes/) |
| [Obtain Auth Tokens](actions/obtain-auth-tokens.md) | `POST /api/v1/auth_token/` | [docs](https://histre.com/features/api/auth/) |
| [Remove Note from Collections](actions/remove-note-from-collections.md) | `POST /api/v1/collections/remove_note/` | [docs](https://histre.com/features/api/collections/) |
| [Retrieve Collection Details](actions/retrieve-collection-details.md) | `GET /api/v1/collections/[:book_id]/` | [docs](https://histre.com/features/api/collections/) |
| [Retrieve a Note](actions/retrieve-note.md) | `GET /api/v1/note/` | [docs](https://histre.com/features/api/notes/) |
| [Retrieve Page Highlights](actions/retrieve-page-highlights.md) | `GET /api/v1/highlight/` | [docs](https://histre.com/features/api/highlights/) |
| [Retrieve Tags](actions/retrieve-tags.md) | `GET /api/v1/tag/` | [docs](https://histre.com/features/api/notes/) |
| [Retrieve User Settings](actions/retrieve-user-settings.md) | `GET /api/v1/settings/` | [docs](https://histre.com/features/api/settings/) |
| [Save Page Highlights](actions/save-page-highlights.md) | `POST /api/v1/highlight/` | [docs](https://histre.com/features/api/highlights/) |
| [Search for Collections](actions/search-collections.md) | `GET /api/v1/collections/search/` | [docs](https://histre.com/features/api/search/) |
| [Search for Highlights](actions/search-highlights.md) | `GET /api/v1/highlight/` | [docs](https://histre.com/features/api/highlights/) |
| [Search Notes](actions/search-notes.md) | `GET /api/v1/notes/` | [docs](https://histre.com/features/api/search/) |
| [Update Collection Details](actions/update-collection-details.md) | `PATCH /api/v1/collections/[:book_id]/` | [docs](https://histre.com/features/api/collections/) |
| [Update a Highlight](actions/update-highlight.md) | `PATCH /api/v1/highlight/` | [docs](https://histre.com/features/api/highlights/) |
