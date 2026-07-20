# Video Indexer (V2) Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Video Indexer (V2) expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/list-videos?connectionId=$CONNECTION_ID&limit=25&offset=0&location=string&accountId=string&accessToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Video Indexer (V2) actions that support pagination

- [List Videos](actions/list-videos.md)
- [Search Videos](actions/search-videos.md)
