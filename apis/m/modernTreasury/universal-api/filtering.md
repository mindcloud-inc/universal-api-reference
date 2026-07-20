# Modern Treasury Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Modern Treasury expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Modern Treasury actions that support filtering

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
