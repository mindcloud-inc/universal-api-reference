# ChargeDesk Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model ChargeDesk expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-agent-activity?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## ChargeDesk actions that support pagination

- [List Agent Activity](actions/list-agent-activity.md)
- [List Charges](actions/list-charges.md)
- [List Customers](actions/list-customers.md)
- [List Products](actions/list-products.md)
- [List Subscription Cancellations](actions/list-subscription-cancellations.md)
- [List Subscriptions](actions/list-subscriptions.md)
