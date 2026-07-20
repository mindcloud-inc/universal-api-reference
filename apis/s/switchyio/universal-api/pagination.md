# Switchy.io Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Switchy.io expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/list-domains?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Switchy.io actions that support pagination

- [List Domains](actions/list-domains.md)
- [List Folders](actions/list-folders.md)
- [List Link Scripts](actions/list-link-scripts.md)
- [List Links](actions/list-links.md)
- [List Pixels](actions/list-pixels.md)
- [List Tokens](actions/list-tokens.md)
- [List UTM Templates](actions/list-utm-templates.md)
