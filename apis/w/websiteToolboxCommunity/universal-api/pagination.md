# Website Toolbox Community Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Website Toolbox Community expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/list-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Website Toolbox Community actions that support pagination

- [List Categories](actions/list-categories.md)
- [List Conversations](actions/list-conversations.md)
- [List Messages](actions/list-messages.md)
- [List Moderators](actions/list-moderators.md)
- [List Page Views](actions/list-page-views.md)
- [List Posts](actions/list-posts.md)
- [List Tags](actions/list-tags.md)
- [List Topics](actions/list-topics.md)
- [List User Groups](actions/list-user-groups.md)
