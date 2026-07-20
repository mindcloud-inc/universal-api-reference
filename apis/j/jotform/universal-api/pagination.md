# Jotform Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Jotform expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jotform/latest/actions/list-form-submissions?connectionId=$CONNECTION_ID&limit=25&offset=0&id=123456789012345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Jotform actions that support pagination

- [List Form Submissions](actions/list-form-submissions.md)
- [List Sub-User Accounts](actions/list-sub-user-accounts.md)
- [List User Forms](actions/list-user-forms.md)
- [List User History](actions/list-user-history.md)
- [List User Invoices](actions/list-user-invoices.md)
- [List User Reports](actions/list-user-reports.md)
- [List User Submissions](actions/list-user-submissions.md)
