# Linkbreakers Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Linkbreakers expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-directories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Linkbreakers actions that support pagination

- [List Directories](actions/list-directories.md)
- [List Events](actions/list-events.md)
- [List Links](actions/list-links.md)
- [List Media Files](actions/list-media-files.md)
- [List Visitors](actions/list-visitors.md)
- [List Workflow Steps for a Link](actions/list-workflow-steps-for-a-link.md)
