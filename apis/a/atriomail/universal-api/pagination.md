# Atriomail Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Atriomail expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/list-catch-alls?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Atriomail actions that support pagination

- [List Catch-Alls](actions/list-catch-alls.md)
- [List Domain Mailboxes](actions/list-domain-mailboxes.md)
- [List Domains](actions/list-domains.md)
- [List Forwarders](actions/list-forwarders.md)
- [List Mailboxes](actions/list-mailboxes.md)
- [List Migrations](actions/list-migrations.md)
- [List Users](actions/list-users.md)
