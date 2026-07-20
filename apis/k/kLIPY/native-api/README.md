# KLIPY: Native API Reference

A consolidated summary of KLIPY's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://docs.klipy.com/getting-started
- **API base URL:** `https://api.klipy.com`

## Authentication

### API Key

Use a KLIPY API key from the Partner Panel.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.klipy.com/getting-started)

## API conventions

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get AI Emoji Items](actions/get-ai-emoji-items.md) | `GET /api/v1/:app_key/emojis/items` | [docs](https://docs.klipy.com/emojis-api/emojis-items-api) |
| [Get Autocomplete Suggestions](actions/get-autocomplete-suggestions.md) | `GET /api/v1/:app_key/autocomplete/:q` | [docs](https://docs.klipy.com/search-suggestions-and-autocomplete/autocomplete) |
| [Get Clip Items](actions/get-clip-items.md) | `GET /api/v1/:app_key/clips/items` | [docs](https://docs.klipy.com/clips-api/clips-items-api) |
| [Get GIF Items](actions/get-gif-items.md) | `GET /api/v1/:app_key/gifs/items` | [docs](https://docs.klipy.com/gifs-api/gifs-items-api) |
| [Get Meme Items](actions/get-meme-items.md) | `GET /api/v1/:app_key/static-memes/items` | [docs](https://docs.klipy.com/memes-api/memes-items-api) |
| [Get Search Suggestions](actions/get-search-suggestions.md) | `GET /api/v1/:app_key/search-suggestions/:q` | [docs](https://docs.klipy.com/search-suggestions-and-autocomplete/search-suggestions) |
| [Get Sticker Items](actions/get-sticker-items.md) | `GET /api/v1/:app_key/stickers/items` | [docs](https://docs.klipy.com/stickers-api/stickers-items-api) |
| [List AI Emoji Categories](actions/list-ai-emoji-categories.md) | `GET /api/v1/:app_key/emojis/categories` | [docs](https://docs.klipy.com/emojis-api/emojis-categories-api) |
| [List Clip Categories](actions/list-clip-categories.md) | `GET /api/v1/:app_key/clips/categories` | [docs](https://docs.klipy.com/clips-api/clips-categories-api) |
| [List GIF Categories](actions/list-gif-categories.md) | `GET /api/v1/:app_key/gifs/categories` | [docs](https://docs.klipy.com/gifs-api/gifs-categories-api) |
| [List Meme Categories](actions/list-meme-categories.md) | `GET /api/v1/:app_key/static-memes/categories` | [docs](https://docs.klipy.com/memes-api/memes-categories-api) |
| [List Sticker Categories](actions/list-sticker-categories.md) | `GET /api/v1/:app_key/stickers/categories` | [docs](https://docs.klipy.com/stickers-api/stickers-categories-api) |
| [List Trending AI Emojis](actions/list-trending-ai-emojis.md) | `GET /api/v1/:app_key/emojis/trending` | [docs](https://docs.klipy.com/emojis-api/emojis-trending-api) |
| [List Trending Clips](actions/list-trending-clips.md) | `GET /api/v1/:app_key/clips/trending` | [docs](https://docs.klipy.com/clips-api/clips-trending-api) |
| [List Trending GIFs](actions/list-trending-gi-fs.md) | `GET /api/v1/:app_key/gifs/trending` | [docs](https://docs.klipy.com/gifs-api/trending-api) |
| [List Trending Memes](actions/list-trending-memes.md) | `GET /api/v1/:app_key/static-memes/trending` | [docs](https://docs.klipy.com/memes-api/memes-trending-api) |
| [List Trending Stickers](actions/list-trending-stickers.md) | `GET /api/v1/:app_key/stickers/trending` | [docs](https://docs.klipy.com/stickers-api/stickers-trending-api) |
| [Search AI Emojis](actions/search-ai-emojis.md) | `GET /api/v1/:app_key/emojis/search` | [docs](https://docs.klipy.com/emojis-api/emojis-search-api) |
| [Search Clips](actions/search-clips.md) | `GET /api/v1/:app_key/clips/search` | [docs](https://docs.klipy.com/clips-api/clips-search-api) |
| [Search GIFs](actions/search-gi-fs.md) | `GET /api/v1/:app_key/gifs/search` | [docs](https://docs.klipy.com/gifs-api/search-api) |
| [Search Memes](actions/search-memes.md) | `GET /api/v1/:app_key/static-memes/search` | [docs](https://docs.klipy.com/memes-api/memes-search-api) |
| [Search Stickers](actions/search-stickers.md) | `GET /api/v1/:app_key/stickers/search` | [docs](https://docs.klipy.com/stickers-api/stickers-search-api) |
