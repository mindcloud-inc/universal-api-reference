# Finmo Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Finmo expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Finmo actions that support pagination

- [List Customers](actions/list-customers.md)
- [List Payins](actions/list-payins.md)
- [List Payout Beneficiaries](actions/list-payout-beneficiaries.md)
- [List Payout Senders](actions/list-payout-senders.md)
- [List Payouts](actions/list-payouts.md)
- [List Refunds](actions/list-refunds.md)
- [List Virtual Accounts](actions/list-virtual-accounts.md)
- [List Wallets](actions/list-wallets.md)
