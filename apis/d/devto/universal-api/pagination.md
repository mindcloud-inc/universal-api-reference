# Dev.to Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Dev.to expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devto/latest/actions/list-all-my-articles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Dev.to actions that support pagination

- [List All My Articles](actions/list-all-my-articles.md)
- [List Followers](actions/list-followers.md)
- [List Latest Articles](actions/list-latest-articles.md)
- [List My Articles](actions/list-my-articles.md)
- [List My Draft Articles](actions/list-my-draft-articles.md)
- [List My Published Articles](actions/list-my-published-articles.md)
- [List Organization Articles](actions/list-organization-articles.md)
- [List Published Articles](actions/list-published-articles.md)
- [List Reading List](actions/list-reading-list.md)
- [List Tags](actions/list-tags.md)
