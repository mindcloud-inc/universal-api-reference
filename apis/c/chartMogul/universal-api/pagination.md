# ChartMogul Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model ChartMogul expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## ChartMogul actions that support pagination

- [List Activities](actions/list-activities.md)
- [List Contacts](actions/list-contacts.md)
- [List Customers](actions/list-customers.md)
- [List Invoices](actions/list-invoices.md)
- [List Notes and Call Logs](actions/list-notes-and-call-logs.md)
- [List Opportunities](actions/list-opportunities.md)
- [List Plan Groups](actions/list-plan-groups.md)
- [List Plans](actions/list-plans.md)
- [List Plans in a Plan Group](actions/list-plans-in-a-plan-group.md)
- [List Subscription Events](actions/list-subscription-events.md)
- [List Tasks](actions/list-tasks.md)
