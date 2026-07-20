# Deskpro Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Deskpro expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-articles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Deskpro actions that support pagination

- [List Articles](actions/list-articles.md)
- [List Guides](actions/list-guides.md)
- [List Organization Tickets](actions/list-organization-tickets.md)
- [List Organizations](actions/list-organizations.md)
- [List People](actions/list-people.md)
- [List Person Tickets](actions/list-person-tickets.md)
- [List Ticket Approvals](actions/list-ticket-approvals.md)
- [List Ticket Filter Tickets](actions/list-ticket-filter-tickets.md)
- [List Ticket Filters](actions/list-ticket-filters.md)
- [List Ticket IDs](actions/list-ticket-ids.md)
- [List Ticket Logs](actions/list-ticket-logs.md)
- [List Ticket Messages](actions/list-ticket-messages.md)
- [List Tickets](actions/list-tickets.md)
