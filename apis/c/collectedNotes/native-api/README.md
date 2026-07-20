# Collected Notes: Native API Reference

A consolidated summary of Collected Notes's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://collectednotes.com/blog/api
- **API base URL:** `https://collectednotes.com`

## Authentication

### API Key

Connect with a Collected Notes API token.

### Credentials

- **API Key:** `apiKey` · required
- **Email:** `email` · required · Collected Notes account email used in the Authorization header.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://collectednotes.com/blog/api#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | `POST /sites/:siteId/notes` | [docs](https://collectednotes.com/blog/api#create-a-note) |
| [Create Note in First Site](actions/create-note-in-first-site.md) | `POST /notes/add` | [docs](https://collectednotes.com/blog/api#create-a-note-simplified) |
| [Create Site](actions/create-site.md) | `POST /sites` | [docs](https://collectednotes.com/blog/api#create-a-site) |
| [Delete Note](actions/delete-note.md) | `DELETE /sites/:siteId/notes/:noteId` | [docs](https://collectednotes.com/blog/api#delete-a-note) |
| [Get Current User](actions/get-current-user.md) | `GET /accounts/me` | [docs](https://collectednotes.com/blog/api#fetch-your-user) |
| [Get Note JSON](actions/get-note-json.md) | `GET /:sitePath/:notePath.json` | [docs](https://collectednotes.com/blog/api#you-can-get-a-note-in-different-formats) |
| [Get Note Links HTML](actions/get-note-links-html.md) | `GET /sites/:siteId/notes/:noteId/links` | [docs](https://collectednotes.com/blog/api#note-links) |
| [Get Note Markdown](actions/get-note-markdown.md) | `GET /:sitePath/:notePath.md` | [docs](https://collectednotes.com/blog/api#you-can-get-a-note-in-different-formats) |
| [Get Note Text](actions/get-note-text.md) | `GET /:sitePath/:notePath.text` | [docs](https://collectednotes.com/blog/api#you-can-get-a-note-in-different-formats) |
| [Get Rendered Note Body](actions/get-rendered-note-body.md) | `GET /sites/:siteId/notes/:noteId/body` | [docs](https://collectednotes.com/blog/api#get-the-rendered-body-of-a-note) |
| [Get Site](actions/get-site.md) | `GET /:sitePath` | [docs](https://collectednotes.com/blog/api#fetch-a-site) |
| [Get Site JSON](actions/get-site-json.md) | `GET /:sitePath.json` | [docs](https://collectednotes.com/blog/api#fetch-your-sites) |
| [Get Site Markdown](actions/get-site-markdown.md) | `GET /:sitePath.md` | [docs](https://collectednotes.com/blog/api#fetch-your-sites) |
| [Get Site RSS Feed](actions/get-site-rss-feed.md) | `GET /:sitePath.rss` | [docs](https://collectednotes.com/blog/api#fetch-your-sites) |
| [List Note Links](actions/list-note-links.md) | `GET /sites/:siteId/notes/:noteId/links.json` | [docs](https://collectednotes.com/blog/api#note-links) |
| [List Note References](actions/list-note-references.md) | `GET /sites/:siteId/notes/:noteId/references.json` | [docs](https://collectednotes.com/blog/api#note-references) |
| [List Notes](actions/list-notes.md) | `GET /sites/:siteId/notes` | [docs](https://collectednotes.com/blog/api#fetch-latest-notes-from-a-site) |
| [List Sites](actions/list-sites.md) | `GET /sites` | [docs](https://collectednotes.com/blog/api#fetch-your-sites) |
| [Reorder Notes](actions/reorder-notes.md) | `GET /sites/:siteId/notes/reorder` | [docs](https://collectednotes.com/blog/api#reorder-notes) |
| [Search Notes](actions/search-notes.md) | `GET /sites/:siteId/notes/search` | [docs](https://collectednotes.com/blog/api#search-notes) |
| [Update Note](actions/update-note.md) | `PUT /sites/:siteId/notes/:noteId` | [docs](https://collectednotes.com/blog/api#update-a-note) |
