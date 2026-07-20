# Perigon Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Perigon expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perigon/latest/actions/get-story-counts?connectionId=$CONNECTION_ID&limit=25&offset=0&splitBy=DAY" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Perigon actions that support pagination

- [Get Story Counts](actions/get-story-counts.md)
- [Get Story History](actions/get-story-history.md)
- [Search Articles](actions/search-articles.md)
- [Search Companies](actions/search-companies.md)
- [Search Journalists](actions/search-journalists.md)
- [Search People](actions/search-people.md)
- [Search Sources](actions/search-sources.md)
- [Search Stories](actions/search-stories.md)
- [Search Summarizer](actions/search-summarizer.md)
- [Search Topics](actions/search-topics.md)
- [Search Wikipedia](actions/search-wikipedia.md)
