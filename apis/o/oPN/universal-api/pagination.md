# OPN Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model OPN expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/list-chain-keys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## OPN actions that support pagination

- [List Chain Keys](actions/list-chain-keys.md)
- [List Chains](actions/list-chains.md)
- [List Charge Events](actions/list-charge-events.md)
- [List Charge Refunds](actions/list-charge-refunds.md)
- [List Charge Schedules](actions/list-charge-schedules.md)
- [List Charges](actions/list-charges.md)
- [List Closed Disputes](actions/list-closed-disputes.md)
- [List Customer Cards](actions/list-customer-cards.md)
- [List Customer Schedules](actions/list-customer-schedules.md)
- [List Customers](actions/list-customers.md)
- [List Dispute Documents](actions/list-dispute-documents.md)
- [List Disputes](actions/list-disputes.md)
- [List Events](actions/list-events.md)
- [List Link Charges](actions/list-link-charges.md)
- [List Linked Accounts](actions/list-linked-accounts.md)
- [List Links](actions/list-links.md)
- [List Open Disputes](actions/list-open-disputes.md)
- [List Pending Disputes](actions/list-pending-disputes.md)
- [List Receipts](actions/list-receipts.md)
- [List Recipient Schedules](actions/list-recipient-schedules.md)
- [List Recipients](actions/list-recipients.md)
- [List Refunds](actions/list-refunds.md)
- [List Routing Group Rules](actions/list-routing-group-rules.md)
- [List Schedule Occurrences](actions/list-schedule-occurrences.md)
- [List Schedules](actions/list-schedules.md)
- [List Sub Merchants](actions/list-sub-merchants.md)
- [List Transactions](actions/list-transactions.md)
- [List Transfer Schedules](actions/list-transfer-schedules.md)
- [List Transfers](actions/list-transfers.md)
- [List Webhook Secrets](actions/list-webhook-secrets.md)
- [Search Charges](actions/search-charges.md)
- [Search Customers](actions/search-customers.md)
- [Search Links](actions/search-links.md)
