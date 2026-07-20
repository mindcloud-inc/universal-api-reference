# pixx.io Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model pixx.io expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/list-collections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## pixx.io actions that support pagination

- [List Collections](actions/list-collections.md)
- [List Custom Metadata](actions/list-custom-metadata.md)
- [List Direct Links](actions/list-direct-links.md)
- [List Directories](actions/list-directories.md)
- [List External Shares](actions/list-external-shares.md)
- [List Files](actions/list-files.md)
- [List Keywords](actions/list-keywords.md)
- [List Permission Groups](actions/list-permission-groups.md)
- [List Synonyms](actions/list-synonyms.md)
- [List Upload Links](actions/list-upload-links.md)
- [List Users](actions/list-users.md)
