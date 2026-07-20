# RunSensible Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model RunSensible expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runSensible/latest/actions/list-appointments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## RunSensible actions that support pagination

- [List Appointments](actions/list-appointments.md)
- [List Contacts](actions/list-contacts.md)
- [List Invoices](actions/list-invoices.md)
- [List Notes](actions/list-notes.md)
- [List Opportunities](actions/list-opportunities.md)
- [List Projects](actions/list-projects.md)
- [List Quotes](actions/list-quotes.md)
- [List Teams](actions/list-teams.md)
- [List Tickets](actions/list-tickets.md)
