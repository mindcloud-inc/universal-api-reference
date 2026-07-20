# Giphy Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Giphy expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giphy/latest/actions/autocomplete-gif-tags?connectionId=$CONNECTION_ID&limit=25&offset=0&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Giphy actions that support pagination

- [Autocomplete GIF Tags](actions/autocomplete-gif-tags.md)
- [List Emoji](actions/list-emoji.md)
- [List Trending Clips](actions/list-trending-clips.md)
- [List Trending GIFs](actions/list-trending-gifs.md)
- [List Trending Stickers](actions/list-trending-stickers.md)
- [Search Channels](actions/search-channels.md)
- [Search Clips](actions/search-clips.md)
- [Search GIFs](actions/search-gifs.md)
- [Search Stickers](actions/search-stickers.md)
