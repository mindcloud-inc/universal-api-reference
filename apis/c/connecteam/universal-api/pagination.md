# Connecteam Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Connecteam expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-custom-fields?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Connecteam actions that support pagination

- [List Custom Fields](actions/list-custom-fields.md)
- [List Jobs](actions/list-jobs.md)
- [List Tasks](actions/list-tasks.md)
- [List User Balances](actions/list-user-balances.md)
- [List Users](actions/list-users.md)
