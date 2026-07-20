# ScrapFly Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model ScrapFly expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/list-crawled-ur-ls?connectionId=$CONNECTION_ID&limit=25&offset=0&crawlerUuid=bf7282d8-818f-4a17-b3d7-a97a8f49ee65" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## ScrapFly actions that support pagination

- [List Crawled URLs](actions/list-crawled-ur-ls.md)
