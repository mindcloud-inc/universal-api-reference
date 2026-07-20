# <img src="https://images.mindcloud.co/apps/icons/giphy_1773267023659.png" alt="Giphy logo" width="28" height="28"> Giphy: Universal API

Giphy: Search, discover, and share GIFs, stickers, and clips

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/giphy/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://giphy.com
- **Vendor API docs:** https://developers.giphy.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Random ID](actions/get-random-id.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giphy/latest/actions/get-random-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Analytics Event

| Action | Method | Description |
| --- | --- | --- |
| [Register Content Action](actions/register-content-action.md) | POST | Registers a GIF or sticker interaction in Giphy analytics. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List GIF Categories](actions/list-gif-categories.md) | GET | Retrieves GIF categories from Giphy. |

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Search Channels](actions/search-channels.md) | GET | Finds channels in Giphy by search term. |

### Clip

| Action | Method | Description |
| --- | --- | --- |
| [List Trending Clips](actions/list-trending-clips.md) | GET | Retrieves trending clips from Giphy. |
| [Search Clips](actions/search-clips.md) | GET | Finds clips in Giphy by search phrase. |

### Content

| Action | Method | Description |
| --- | --- | --- |
| [Get Content by ID](actions/get-content-by-id.md) | GET | Retrieves GIF, sticker, or clip content from Giphy by ID. |
| [Get Content by IDs](actions/get-content-by-ids.md) | GET | Retrieves GIF, sticker, or clip content from Giphy by IDs. |

### Emoji

| Action | Method | Description |
| --- | --- | --- |
| [Get Emoji Variations](actions/get-emoji-variations.md) | GET | Retrieves emoji variations from Giphy by ID. |
| [List Emoji](actions/list-emoji.md) | GET | Retrieves emoji from Giphy. |

### Gif

| Action | Method | Description |
| --- | --- | --- |
| [Get GIF by ID](actions/get-gif-by-id.md) | GET | Retrieves a GIF from Giphy by ID. |
| [Get GIFs by ID](actions/get-gifs-by-id.md) | GET | Retrieves multiple GIFs from Giphy by ID. |
| [Get Random GIF](actions/get-random-gif.md) | GET | Retrieves a random GIF from Giphy. |
| [List Trending GIFs](actions/list-trending-gifs.md) | GET | Retrieves trending GIFs from Giphy. |
| [Search GIFs](actions/search-gifs.md) | GET | Finds GIFs in Giphy by search phrase. |
| [Translate to GIF](actions/translate-to-gif.md) | GET | Translates a phrase into a GIF in Giphy. |
| [Upload GIF](actions/upload-gif.md) | POST | Uploads a GIF to Giphy. |

### Random Id

| Action | Method | Description |
| --- | --- | --- |
| [Get Random ID](actions/get-random-id.md) | GET | Retrieves a random ID from Giphy. |

### Search Term

| Action | Method | Description |
| --- | --- | --- |
| [List Trending Search Terms](actions/list-trending-search-terms.md) | GET | Retrieves trending search terms from Giphy. |

### Sticker

| Action | Method | Description |
| --- | --- | --- |
| [Get Random Sticker](actions/get-random-sticker.md) | GET | Retrieves a random sticker from Giphy. |
| [List Trending Stickers](actions/list-trending-stickers.md) | GET | Retrieves trending stickers from Giphy. |
| [Search Stickers](actions/search-stickers.md) | GET | Finds stickers in Giphy by search phrase. |
| [Translate to Sticker](actions/translate-to-sticker.md) | GET | Translates a phrase into a sticker in Giphy. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete GIF Tags](actions/autocomplete-gif-tags.md) | GET | Finds autocomplete tag terms for GIFs in Giphy. |
| [Get Related Tag Terms](actions/get-related-tag-terms.md) | GET | Retrieves related tag terms from Giphy by term. |

