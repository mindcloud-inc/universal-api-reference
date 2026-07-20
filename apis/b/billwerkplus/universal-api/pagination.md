# Billwerkplus Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Billwerkplus expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/list-add-ons?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Billwerkplus actions that support pagination

- [List Add-Ons](actions/list-add-ons.md)
- [List Charges](actions/list-charges.md)
- [List Customers](actions/list-customers.md)
- [List Disputes](actions/list-disputes.md)
- [List Invoices](actions/list-invoices.md)
- [List Payment Methods](actions/list-payment-methods.md)
- [List Plans](actions/list-plans.md)
- [List Subscriptions](actions/list-subscriptions.md)
