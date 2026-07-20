# Endear Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Endear expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/endear/latest/actions/list-customer-fields?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Endear actions that support pagination

- [List Customer Fields](actions/list-customer-fields.md)
- [List Integrations](actions/list-integrations.md)
- [List Messages](actions/list-messages.md)
- [List Teams](actions/list-teams.md)
- [List Users](actions/list-users.md)
- [Search Conversations](actions/search-conversations.md)
- [Search Customers](actions/search-customers.md)
- [Search Drafts](actions/search-drafts.md)
- [Search Messages](actions/search-messages.md)
- [Search Notes](actions/search-notes.md)
- [Search Tasks](actions/search-tasks.md)
