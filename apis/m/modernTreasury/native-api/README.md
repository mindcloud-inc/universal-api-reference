# Modern Treasury: Native API Reference

A consolidated summary of Modern Treasury's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.moderntreasury.com/platform/reference
- **OpenAPI specification:** https://raw.githubusercontent.com/Modern-Treasury/modern-treasury-openapi/main/openapi/mt_openapi_spec_v1.yaml
- **API base URL:** `https://app.moderntreasury.com/api`

## Authentication

### Basic Auth

Modern Treasury API authentication using the organization ID as the Basic username and API key as the Basic password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.moderntreasury.com/platform/docs/create-an-api-key)

## API conventions

Responses from this API use JSON. The next-page cursor is read from `meta.response.headers.x-after-cursor`.

## Pagination

Use `per_page` in the query string to set the page size (default 25; accepted range 1–100). Use `after_cursor` in the query string as the pagination cursor; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Account Collection Flows](actions/list-account-collection-flows.md) | `GET /account_collection_flows` | [docs](https://docs.moderntreasury.com/platform/reference/list-account-collection-flows) |
| [List Bulk Requests](actions/list-bulk-requests.md) | `GET /bulk_requests` | [docs](https://docs.moderntreasury.com/platform/reference/list-bulk-requests) |
| [List Bulk Results](actions/list-bulk-results.md) | `GET /bulk_results` | [docs](https://docs.moderntreasury.com/platform/reference/list-bulk-results) |
| [List Connection Legal Entities](actions/list-connection-legal-entities.md) | `GET /connection_legal_entities` | [docs](https://docs.moderntreasury.com/platform/reference/list-connection-legal-entities) |
| [List Connections](actions/list-connections.md) | `GET /connections` | [docs](https://docs.moderntreasury.com/platform/reference/list-connections) |
| [List Counterparties](actions/list-counterparties.md) | `GET /counterparties` | [docs](https://docs.moderntreasury.com/platform/reference/list-counterparties) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://docs.moderntreasury.com/platform/reference/list-documents) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://docs.moderntreasury.com/platform/reference/list-events) |
| [List Expected Payments](actions/list-expected-payments.md) | `GET /expected_payments` | [docs](https://docs.moderntreasury.com/platform/reference/list-expected-payments) |
| [List External Accounts](actions/list-external-accounts.md) | `GET /external_accounts` | [docs](https://docs.moderntreasury.com/platform/reference/list-external-accounts) |
| [List Foreign Exchange Quotes](actions/list-foreign-exchange-quotes.md) | `GET /foreign_exchange_quotes` | [docs](https://docs.moderntreasury.com/platform/reference/list-quotes) |
| [List Incoming Payment Details](actions/list-incoming-payment-details.md) | `GET /incoming_payment_details` | [docs](https://docs.moderntreasury.com/platform/reference/list-incoming-payment-details) |
| [List Internal Accounts](actions/list-internal-accounts.md) | `GET /internal_accounts` | [docs](https://docs.moderntreasury.com/platform/reference/list-internal-accounts) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://docs.moderntreasury.com/platform/reference/list-invoices) |
| [List Ledger Account Balance Monitors](actions/list-ledger-account-balance-monitors.md) | `GET /ledger_account_balance_monitors` | [docs](https://docs.moderntreasury.com/platform/reference/list-ledger-account-balance-monitors) |
| [List Ledger Account Categories](actions/list-ledger-account-categories.md) | `GET /ledger_account_categories` | [docs](https://docs.moderntreasury.com/platform/reference/list-ledger-account-categories) |
| [List Ledger Account Settlements](actions/list-ledger-account-settlements.md) | `GET /ledger_account_settlements` | [docs](https://docs.moderntreasury.com/platform/reference/list-ledger-account-settlements) |
| [List Ledger Accounts](actions/list-ledger-accounts.md) | `GET /ledger_accounts` | [docs](https://docs.moderntreasury.com/platform/reference/list-ledger-accounts) |
| [List Ledger Entries](actions/list-ledger-entries.md) | `GET /ledger_entries` | [docs](https://docs.moderntreasury.com/platform/reference/list-ledger-entries) |
| [List Ledger Transactions](actions/list-ledger-transactions.md) | `GET /ledger_transactions` | [docs](https://docs.moderntreasury.com/platform/reference/list-ledger-transactions) |
| [List Ledgers](actions/list-ledgers.md) | `GET /ledgers` | [docs](https://docs.moderntreasury.com/platform/reference/list-ledgers) |
| [List Legal Entities](actions/list-legal-entities.md) | `GET /legal_entities` | [docs](https://docs.moderntreasury.com/platform/reference/list-legal-entities) |
| [List Payment Actions](actions/list-payment-actions.md) | `GET /payment_actions` | [docs](https://docs.moderntreasury.com/platform/reference/list-payment-actions) |
| [List Payment Flows](actions/list-payment-flows.md) | `GET /payment_flows` | [docs](https://docs.moderntreasury.com/platform/reference/list-payment-flows) |
| [List Payment Orders](actions/list-payment-orders.md) | `GET /payment_orders` | [docs](https://docs.moderntreasury.com/platform/reference/list-payment-orders) |
| [List Payment References](actions/list-payment-references.md) | `GET /payment_references` | [docs](https://docs.moderntreasury.com/platform/reference/list-payment-references) |
| [List Returns](actions/list-returns.md) | `GET /returns` | [docs](https://docs.moderntreasury.com/platform/reference/list-returns) |
| [List Transaction Line Items](actions/list-transaction-line-items.md) | `GET /transaction_line_items` | [docs](https://docs.moderntreasury.com/platform/reference/list-transaction-line-items) |
| [List Transactions](actions/list-transactions.md) | `GET /transactions` | [docs](https://docs.moderntreasury.com/platform/reference/list-transactions) |
| [List Virtual Accounts](actions/list-virtual-accounts.md) | `GET /virtual_accounts` | [docs](https://docs.moderntreasury.com/platform/reference/list-virtual-accounts) |
