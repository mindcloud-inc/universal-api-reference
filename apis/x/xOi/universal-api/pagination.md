# XOi Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model XOi expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xOi/latest/actions/list-content-webhook-history?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## XOi actions that support pagination

- [List Content Webhook History](actions/list-content-webhook-history.md)
- [List Jobs](actions/list-jobs.md)
- [List Jobs by Customer Name](actions/list-jobs-by-customer-name.md)
- [List Jobs by Date Range](actions/list-jobs-by-date-range.md)
- [List Jobs by Job Location](actions/list-jobs-by-job-location.md)
- [List Jobs by Work Order](actions/list-jobs-by-work-order.md)
- [List Jobs Webhook History](actions/list-jobs-webhook-history.md)
- [List Users](actions/list-users.md)
- [Search Knowledge Base](actions/search-knowledge-base.md)
