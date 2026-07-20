# <img src="https://images.mindcloud.co/apps/icons/75ba7dbb-9da9-4c76-8e3a-4a9540cb7fd0-8_1775841730218.png" alt="KLIPY logo" width="28" height="28"> KLIPY: Universal API

Search, browse, and share KLIPY GIFs, stickers, clips, and memes

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kLIPY/latest
- **Category:** Marketing / Social Media
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://klipy.com/
- **Vendor API docs:** https://docs.klipy.com/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List GIF Categories](actions/list-gif-categories.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kLIPY/latest/actions/list-gif-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Ai Emoji

| Action | Method | Description |
| --- | --- | --- |
| [Get AI Emoji Items](actions/get-ai-emoji-items.md) | GET | Retrieves AI emojis from KLIPY by ID or slug. |
| [List Trending AI Emojis](actions/list-trending-ai-emojis.md) | GET | Retrieves trending AI emojis from KLIPY. |
| [Search AI Emojis](actions/search-ai-emojis.md) | GET | Finds AI emojis in KLIPY by search term. |

### Ai Emoji Category

| Action | Method | Description |
| --- | --- | --- |
| [List AI Emoji Categories](actions/list-ai-emoji-categories.md) | GET | Retrieves available AI emoji categories from KLIPY. |

### Autocomplete Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Get Autocomplete Suggestions](actions/get-autocomplete-suggestions.md) | GET | Retrieves autocomplete suggestions from KLIPY for a query. |

### Clip

| Action | Method | Description |
| --- | --- | --- |
| [Get Clip Items](actions/get-clip-items.md) | GET | Retrieves clips from KLIPY by ID or slug. |
| [List Trending Clips](actions/list-trending-clips.md) | GET | Retrieves current trending clips from KLIPY. |
| [Search Clips](actions/search-clips.md) | GET | Finds clips in KLIPY by search term. |

### Clip Category

| Action | Method | Description |
| --- | --- | --- |
| [List Clip Categories](actions/list-clip-categories.md) | GET | Retrieves available clip categories from KLIPY. |

### Gif

| Action | Method | Description |
| --- | --- | --- |
| [Get GIF Items](actions/get-gif-items.md) | GET | Retrieves GIFs from KLIPY by ID or slug. |
| [List Trending GIFs](actions/list-trending-gi-fs.md) | GET | Retrieves current trending GIFs from KLIPY. |
| [Search GIFs](actions/search-gi-fs.md) | GET | Finds GIFs in KLIPY by search term. |

### Gif Category

| Action | Method | Description |
| --- | --- | --- |
| [List GIF Categories](actions/list-gif-categories.md) | GET | Retrieves available GIF categories from KLIPY. |

### Meme

| Action | Method | Description |
| --- | --- | --- |
| [Get Meme Items](actions/get-meme-items.md) | GET | Retrieves memes from KLIPY by ID or slug. |
| [List Trending Memes](actions/list-trending-memes.md) | GET | Retrieves current trending memes from KLIPY. |
| [Search Memes](actions/search-memes.md) | GET | Finds memes in KLIPY by search term. |

### Meme Category

| Action | Method | Description |
| --- | --- | --- |
| [List Meme Categories](actions/list-meme-categories.md) | GET | Retrieves available meme categories from KLIPY. |

### Search Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Get Search Suggestions](actions/get-search-suggestions.md) | GET | Retrieves search suggestions from KLIPY for a query. |

### Sticker

| Action | Method | Description |
| --- | --- | --- |
| [Get Sticker Items](actions/get-sticker-items.md) | GET | Retrieves stickers from KLIPY by ID or slug. |
| [List Trending Stickers](actions/list-trending-stickers.md) | GET | Retrieves current trending stickers from KLIPY. |
| [Search Stickers](actions/search-stickers.md) | GET | Finds stickers in KLIPY by search term. |

### Sticker Category

| Action | Method | Description |
| --- | --- | --- |
| [List Sticker Categories](actions/list-sticker-categories.md) | GET | Retrieves available sticker categories from KLIPY. |

