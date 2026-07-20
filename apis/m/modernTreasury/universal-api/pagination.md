# Modern Treasury Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Modern Treasury expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-account-collection-flows?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Modern Treasury actions that support pagination

- [List Account Collection Flows](actions/list-account-collection-flows.md)
- [List Bulk Requests](actions/list-bulk-requests.md)
- [List Bulk Results](actions/list-bulk-results.md)
- [List Connection Legal Entities](actions/list-connection-legal-entities.md)
- [List Connections](actions/list-connections.md)
- [List Counterparties](actions/list-counterparties.md)
- [List Documents](actions/list-documents.md)
- [List Events](actions/list-events.md)
- [List Expected Payments](actions/list-expected-payments.md)
- [List External Accounts](actions/list-external-accounts.md)
- [List Foreign Exchange Quotes](actions/list-foreign-exchange-quotes.md)
- [List Incoming Payment Details](actions/list-incoming-payment-details.md)
- [List Internal Accounts](actions/list-internal-accounts.md)
- [List Invoices](actions/list-invoices.md)
- [List Ledger Account Balance Monitors](actions/list-ledger-account-balance-monitors.md)
- [List Ledger Account Categories](actions/list-ledger-account-categories.md)
- [List Ledger Account Settlements](actions/list-ledger-account-settlements.md)
- [List Ledger Accounts](actions/list-ledger-accounts.md)
- [List Ledger Entries](actions/list-ledger-entries.md)
- [List Ledger Transactions](actions/list-ledger-transactions.md)
- [List Ledgers](actions/list-ledgers.md)
- [List Legal Entities](actions/list-legal-entities.md)
- [List Payment Actions](actions/list-payment-actions.md)
- [List Payment Flows](actions/list-payment-flows.md)
- [List Payment Orders](actions/list-payment-orders.md)
- [List Payment References](actions/list-payment-references.md)
- [List Returns](actions/list-returns.md)
- [List Transaction Line Items](actions/list-transaction-line-items.md)
- [List Transactions](actions/list-transactions.md)
- [List Virtual Accounts](actions/list-virtual-accounts.md)
