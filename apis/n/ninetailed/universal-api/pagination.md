# Ninetailed Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Ninetailed expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/list-assets?connectionId=$CONNECTION_ID&limit=25&offset=0&spaceId=string&environmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Ninetailed actions that support pagination

- [List Assets](actions/list-assets.md)
- [List Content Types](actions/list-content-types.md)
- [List Entries](actions/list-entries.md)
- [List Environments](actions/list-environments.md)
- [List Published Entries](actions/list-published-entries.md)
- [List Roles](actions/list-roles.md)
- [List Tags](actions/list-tags.md)
- [List Webhooks](actions/list-webhooks.md)
