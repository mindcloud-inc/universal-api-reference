# Instapaper: Native API Reference

A consolidated summary of Instapaper's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://www.instapaper.com/developers/v1/full-api
- **API base URL:** `https://www.instapaper.com`

## Authentication

### OAuth 1.0a

Connect Instapaper using OAuth 1.0a consumer credentials and one-time xAuth token minting for the target account.

### Credentials

- **Consumer Key:** `consumerKey` · required
- **Consumer Secret:** `consumerSecret` · required
- **Realm:** `realm` · optional
- **Email or Username:** `username` · required · The Instapaper account username. Instapaper recommends labeling this field as email or username because usernames are not always email addresses.
- **Password, if you have one:** `password` · optional · Only required when the Instapaper account has a password. Instapaper allows blank password values for accounts without one.

OAuth 1.0a signs every request with the consumer key and secret plus the access token and token secret. Use an OAuth 1.0a client library to construct the `Authorization` header; the signature depends on the HTTP method, URL, and request parameters and should not be assembled as a static token.

[Official authentication documentation](https://www.instapaper.com/developers/v1/full-api)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Bookmark](actions/add-bookmark.md) | `POST /api/1/bookmarks/add` | [docs](https://www.instapaper.com/developers/v1/full-api) |
| [Archive Bookmark](actions/archive-bookmark.md) | `POST /api/1/bookmarks/archive` | [docs](https://www.instapaper.com/developers/v1/full-api) |
| [Create Bookmark Highlight](actions/create-bookmark-highlight.md) | `POST /api/1.1/bookmarks/:bookmarkId/highlight` | [docs](https://www.instapaper.com/developers/v1/full-api) |
| [Create Folder](actions/create-folder.md) | `POST /api/1/folders/add` | [docs](https://www.instapaper.com/developers/v1/full-api) |
| [Delete Bookmark](actions/delete-bookmark.md) | `POST /api/1/bookmarks/delete` | [docs](https://www.instapaper.com/developers/v1/full-api) |
| [Delete Folder](actions/delete-folder.md) | `POST /api/1/folders/delete` | [docs](https://www.instapaper.com/developers/v1/full-api) |
| [Delete Highlight](actions/delete-highlight.md) | `POST /api/1.1/highlights/:highlightId/delete` | [docs](https://www.instapaper.com/developers/v1/full-api) |
| [Get Bookmark Text](actions/get-bookmark-text.md) | `POST /api/1/bookmarks/get_text` | [docs](https://www.instapaper.com/developers/v1/full-api) |
| [List Bookmark Highlights](actions/list-bookmark-highlights.md) | `POST /api/1.1/bookmarks/:bookmarkId/highlights` | [docs](https://www.instapaper.com/developers/v1/full-api) |
| [List Bookmarks](actions/list-bookmarks.md) | `POST /api/1/bookmarks/list` | [docs](https://www.instapaper.com/developers/v1/full-api) |
| [List Folders](actions/list-folders.md) | `POST /api/1/folders/list` | [docs](https://www.instapaper.com/developers/v1/full-api) |
| [Move Bookmark](actions/move-bookmark.md) | `POST /api/1/bookmarks/move` | [docs](https://www.instapaper.com/developers/v1/full-api) |
| [Reorder Folders](actions/reorder-folders.md) | `POST /api/1/folders/set_order` | [docs](https://www.instapaper.com/developers/v1/full-api) |
| [Star Bookmark](actions/star-bookmark.md) | `POST /api/1/bookmarks/star` | [docs](https://www.instapaper.com/developers/v1/full-api) |
| [Unarchive Bookmark](actions/unarchive-bookmark.md) | `POST /api/1/bookmarks/unarchive` | [docs](https://www.instapaper.com/developers/v1/full-api) |
| [Unstar Bookmark](actions/unstar-bookmark.md) | `POST /api/1/bookmarks/unstar` | [docs](https://www.instapaper.com/developers/v1/full-api) |
| [Update Bookmark Read Progress](actions/update-bookmark-read-progress.md) | `POST /api/1/bookmarks/update_read_progress` | [docs](https://www.instapaper.com/developers/v1/full-api) |
| [Verify Credentials](actions/verify-credentials.md) | `POST /api/1/account/verify_credentials` | [docs](https://www.instapaper.com/developers/v1/full-api) |
