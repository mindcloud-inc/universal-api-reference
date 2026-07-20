# Giphy: Native API Reference

A consolidated summary of Giphy's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.giphy.com/docs/api
- **API base URL:** `https://api.giphy.com/`

## Authentication

### API Key

Connect to Giphy with an API key from the GIPHY Developer Dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.giphy.com/docs/api/#quick-start-guide)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 25). Use `offset` in the query string as the record offset.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Autocomplete GIF Tags](actions/autocomplete-gif-tags.md) | `GET /v1/gifs/search/tags` | [docs](https://developers.giphy.com/docs/api/endpoint/#autocomplete) |
| [Get Content by ID](actions/get-content-by-id.md) | `GET /v1/content/:id` | [docs](https://developers.giphy.com/docs/clips/endpoint/#get-by-id) |
| [Get Content by IDs](actions/get-content-by-ids.md) | `GET /v1/content` | [docs](https://developers.giphy.com/docs/clips/endpoint/#get-by-ids) |
| [Get Emoji Variations](actions/get-emoji-variations.md) | `GET /v2/emoji/:emojiId/variations` | [docs](https://developers.giphy.com/docs/api/endpoint/#emoji-variations) |
| [Get GIF by ID](actions/get-gif-by-id.md) | `GET /v1/gifs/:gifId` | [docs](https://developers.giphy.com/docs/api/endpoint/#get-gif-by-id) |
| [Get GIFs by ID](actions/get-gifs-by-id.md) | `GET /v1/gifs` | [docs](https://developers.giphy.com/docs/api/endpoint/#get-gifs-by-id) |
| [Get Random GIF](actions/get-random-gif.md) | `GET /v1/gifs/random` | [docs](https://developers.giphy.com/docs/api/endpoint/#random) |
| [Get Random ID](actions/get-random-id.md) | `GET /v1/randomid` | [docs](https://developers.giphy.com/docs/api/endpoint/#random-id) |
| [Get Random Sticker](actions/get-random-sticker.md) | `GET /v1/stickers/random` | [docs](https://developers.giphy.com/docs/api/endpoint/#random) |
| [Get Related Tag Terms](actions/get-related-tag-terms.md) | `GET /v1/tags/related/:term` | [docs](https://developers.giphy.com/docs/api/endpoint/#search-suggestions) |
| [List Emoji](actions/list-emoji.md) | `GET /v2/emoji` | [docs](https://developers.giphy.com/docs/api/endpoint/#emoji) |
| [List GIF Categories](actions/list-gif-categories.md) | `GET /v1/gifs/categories` | [docs](https://developers.giphy.com/docs/api/endpoint/#categories) |
| [List Trending Clips](actions/list-trending-clips.md) | `GET /v1/clips/trending` | [docs](https://developers.giphy.com/docs/clips/endpoint/#trending) |
| [List Trending GIFs](actions/list-trending-gifs.md) | `GET /v1/gifs/trending` | [docs](https://developers.giphy.com/docs/api/endpoint/#trending) |
| [List Trending Search Terms](actions/list-trending-search-terms.md) | `GET /v1/trending/searches` | [docs](https://developers.giphy.com/docs/api/endpoint/#trending-search-terms) |
| [List Trending Stickers](actions/list-trending-stickers.md) | `GET /v1/stickers/trending` | [docs](https://developers.giphy.com/docs/api/endpoint/#trending) |
| [Register Content Action](actions/register-content-action.md) | `GET https://giphy-analytics.giphy.com/v2/pingback_simple` | [docs](https://developers.giphy.com/docs/api/endpoint/#action-register) |
| [Search Channels](actions/search-channels.md) | `GET /v1/channels/search` | [docs](https://developers.giphy.com/docs/api/endpoint/#channel-search) |
| [Search Clips](actions/search-clips.md) | `GET /v1/clips/search` | [docs](https://developers.giphy.com/docs/clips/endpoint/#search) |
| [Search GIFs](actions/search-gifs.md) | `GET /v1/gifs/search` | [docs](https://developers.giphy.com/docs/api/endpoint/#search) |
| [Search Stickers](actions/search-stickers.md) | `GET /v1/stickers/search` | [docs](https://developers.giphy.com/docs/api/endpoint/#search) |
| [Translate to GIF](actions/translate-to-gif.md) | `GET /v1/gifs/translate` | [docs](https://developers.giphy.com/docs/api/endpoint/#translate) |
| [Translate to Sticker](actions/translate-to-sticker.md) | `GET /v1/stickers/translate` | [docs](https://developers.giphy.com/docs/api/endpoint/#translate) |
| [Upload GIF](actions/upload-gif.md) | `POST https://upload.giphy.com/v1/gifs` | [docs](https://developers.giphy.com/docs/api/endpoint/#upload) |
