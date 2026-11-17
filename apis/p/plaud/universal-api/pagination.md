# Plaud AI Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Plaud AI expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plaud/latest/actions/get-transcript?connectionId=$CONNECTION_ID&limit=25&offset=0&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Plaud AI actions that support pagination

- [Get Transcript](actions/get-transcript.md)
- [List Recordings](actions/list-recordings.md)
