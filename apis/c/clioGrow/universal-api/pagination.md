# Clio Grow Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Clio Grow expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/list-contact-notes?connectionId=$CONNECTION_ID&limit=25&offset=0&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Clio Grow actions that support pagination

- [List Contact Notes](actions/list-contact-notes.md)
- [List Contacts](actions/list-contacts.md)
- [List Custom Actions](actions/list-custom-actions.md)
- [List Inbox Leads](actions/list-inbox-leads.md)
- [List Matter Notes](actions/list-matter-notes.md)
- [List Matters](actions/list-matters.md)
- [List Users](actions/list-users.md)
