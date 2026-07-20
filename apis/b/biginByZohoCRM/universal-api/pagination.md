# Bigin by Zoho CRM Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Bigin by Zoho CRM expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/list-deleted-records?connectionId=$CONNECTION_ID&limit=25&offset=0&moduleApiName=Accounts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Bigin by Zoho CRM actions that support pagination

- [List Deleted Records](actions/list-deleted-records.md)
- [List Notes](actions/list-notes.md)
- [List Record Attachments](actions/list-record-attachments.md)
- [List Record Notes](actions/list-record-notes.md)
- [List Records](actions/list-records.md)
- [List Related Records](actions/list-related-records.md)
- [List Users](actions/list-users.md)
