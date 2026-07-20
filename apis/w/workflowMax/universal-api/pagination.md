# WorkflowMax Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model WorkflowMax expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## WorkflowMax actions that support pagination

- [List Clients](actions/list-clients.md)
- [List Invoices](actions/list-invoices.md)
- [List Job Costs](actions/list-job-costs.md)
- [List Job Tasks](actions/list-job-tasks.md)
- [List Jobs](actions/list-jobs.md)
- [List Payments](actions/list-payments.md)
- [List Purchase Order Bills](actions/list-purchase-order-bills.md)
- [List Purchase Orders](actions/list-purchase-orders.md)
- [List Quotes](actions/list-quotes.md)
- [List Suppliers](actions/list-suppliers.md)
- [List Tasks](actions/list-tasks.md)
- [List Timesheets](actions/list-timesheets.md)
