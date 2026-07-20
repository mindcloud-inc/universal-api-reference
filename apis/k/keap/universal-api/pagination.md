# Keap Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Keap expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keap/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Keap actions that support pagination

- [List Companies](actions/list-companies.md)
- [List Contacts](actions/list-contacts.md)
- [List Emails](actions/list-emails.md)
- [List Files](actions/list-files.md)
- [List Notes](actions/list-notes.md)
- [List Opportunities](actions/list-opportunities.md)
- [List Tags](actions/list-tags.md)
- [List Tasks](actions/list-tasks.md)
