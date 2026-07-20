# vionvi CRM Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model vionvi CRM expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vionviCRM/latest/actions/list-catalog-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## vionvi CRM actions that support pagination

- [List Catalog Items](actions/list-catalog-items.md)
- [List Chats](actions/list-chats.md)
- [List Clients](actions/list-clients.md)
- [List Contracts](actions/list-contracts.md)
- [List Funnels](actions/list-funnels.md)
- [List Leads](actions/list-leads.md)
- [List Organizations](actions/list-organizations.md)
- [List Payments](actions/list-payments.md)
- [List Permissions](actions/list-permissions.md)
- [List Projects](actions/list-projects.md)
- [List Roles](actions/list-roles.md)
- [List Services](actions/list-services.md)
- [List Sources](actions/list-sources.md)
- [List Tasks](actions/list-tasks.md)
- [List Users](actions/list-users.md)
