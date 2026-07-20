# CDC Content Services Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model CDC Content Services expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cDCContentServices/latest/actions/list-audiences?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## CDC Content Services actions that support pagination

- [List Audiences](actions/list-audiences.md)
- [List Languages](actions/list-languages.md)
- [List Media](actions/list-media.md)
- [List Media By Tag](actions/list-media-by-tag.md)
- [List Media Types](actions/list-media-types.md)
- [List Organization Types](actions/list-organization-types.md)
- [List Organizations](actions/list-organizations.md)
- [List Sources](actions/list-sources.md)
- [List Tag Types](actions/list-tag-types.md)
- [List Tags](actions/list-tags.md)
- [List Topics](actions/list-topics.md)
