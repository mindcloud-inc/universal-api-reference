# Close Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Close expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/close/latest/actions/list-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Close actions that support pagination

- [List Activities](actions/list-activities.md)
- [List Contacts](actions/list-contacts.md)
- [List Email Templates](actions/list-email-templates.md)
- [List Leads](actions/list-leads.md)
- [List Opportunities](actions/list-opportunities.md)
- [List SMS Templates](actions/list-sms-templates.md)
- [List Tasks](actions/list-tasks.md)
- [List Users](actions/list-users.md)
