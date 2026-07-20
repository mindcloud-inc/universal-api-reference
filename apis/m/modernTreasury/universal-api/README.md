# <img src="https://images.mindcloud.co/apps/icons/images-27_1776872536807.png" alt="Modern Treasury logo" width="28" height="28"> Modern Treasury: Universal API

Modern Treasury provides treasury and payment operations APIs for accounts, counterparties, payment orders, ledgers, reconciliations, documents, events, and related financial workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/modernTreasury/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.moderntreasury.com
- **Vendor API docs:** https://docs.moderntreasury.com/platform/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Internal Accounts](actions/list-internal-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-internal-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Account Collection Flow

| Action | Method | Description |
| --- | --- | --- |
| [List Account Collection Flows](actions/list-account-collection-flows.md) | GET | Retrieves account collection flows from Modern Treasury. |

### Bulk Request

| Action | Method | Description |
| --- | --- | --- |
| [List Bulk Requests](actions/list-bulk-requests.md) | GET | Retrieves bulk requests from Modern Treasury. |

### Bulk Result

| Action | Method | Description |
| --- | --- | --- |
| [List Bulk Results](actions/list-bulk-results.md) | GET | Retrieves bulk results from Modern Treasury. |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [List Connections](actions/list-connections.md) | GET | Retrieves connections from Modern Treasury. |

### Connection Legal Entity

| Action | Method | Description |
| --- | --- | --- |
| [List Connection Legal Entities](actions/list-connection-legal-entities.md) | GET | Retrieves connection legal entities from Modern Treasury. |

### Counterparty

| Action | Method | Description |
| --- | --- | --- |
| [List Counterparties](actions/list-counterparties.md) | GET | Retrieves counterparties from Modern Treasury. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from Modern Treasury. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET | Retrieves events from Modern Treasury. |

### Expected Payment

| Action | Method | Description |
| --- | --- | --- |
| [List Expected Payments](actions/list-expected-payments.md) | GET | Retrieves expected payments from Modern Treasury. |

### External Account

| Action | Method | Description |
| --- | --- | --- |
| [List External Accounts](actions/list-external-accounts.md) | GET | Retrieves external accounts from Modern Treasury. |

### Foreign Exchange Quote

| Action | Method | Description |
| --- | --- | --- |
| [List Foreign Exchange Quotes](actions/list-foreign-exchange-quotes.md) | GET |  |

### Incoming Payment Detail

| Action | Method | Description |
| --- | --- | --- |
| [List Incoming Payment Details](actions/list-incoming-payment-details.md) | GET | Retrieves incoming payment details from Modern Treasury. |

### Internal Account

| Action | Method | Description |
| --- | --- | --- |
| [List Internal Accounts](actions/list-internal-accounts.md) | GET | Retrieves internal accounts from Modern Treasury. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Modern Treasury. |

### Ledger

| Action | Method | Description |
| --- | --- | --- |
| [List Ledgers](actions/list-ledgers.md) | GET | Retrieves ledgers from Modern Treasury. |

### Ledger Account

| Action | Method | Description |
| --- | --- | --- |
| [List Ledger Accounts](actions/list-ledger-accounts.md) | GET | Retrieves ledger accounts from Modern Treasury. |

### Ledger Account Balance Monitor

| Action | Method | Description |
| --- | --- | --- |
| [List Ledger Account Balance Monitors](actions/list-ledger-account-balance-monitors.md) | GET | Retrieves ledger account balance monitors from Modern Treasury. |

### Ledger Account Category

| Action | Method | Description |
| --- | --- | --- |
| [List Ledger Account Categories](actions/list-ledger-account-categories.md) | GET | Retrieves ledger account categories from Modern Treasury. |

### Ledger Account Settlement

| Action | Method | Description |
| --- | --- | --- |
| [List Ledger Account Settlements](actions/list-ledger-account-settlements.md) | GET | Retrieves ledger account settlements from Modern Treasury. |

### Ledger Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Ledger Entries](actions/list-ledger-entries.md) | GET | Retrieves ledger entries from Modern Treasury. |

### Ledger Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Ledger Transactions](actions/list-ledger-transactions.md) | GET | Retrieves ledger transactions from Modern Treasury. |

### Legal Entity

| Action | Method | Description |
| --- | --- | --- |
| [List Legal Entities](actions/list-legal-entities.md) | GET | Retrieves legal entities from Modern Treasury. |

### Payment Action

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Actions](actions/list-payment-actions.md) | GET | Retrieves payment actions from Modern Treasury. |

### Payment Flow

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Flows](actions/list-payment-flows.md) | GET | Retrieves payment flows from Modern Treasury. |

### Payment Order

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Orders](actions/list-payment-orders.md) | GET | Retrieves payment orders from Modern Treasury. |

### Payment Reference

| Action | Method | Description |
| --- | --- | --- |
| [List Payment References](actions/list-payment-references.md) | GET | Retrieves payment references from Modern Treasury. |

### Return

| Action | Method | Description |
| --- | --- | --- |
| [List Returns](actions/list-returns.md) | GET | Retrieves returns from Modern Treasury. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves transactions from Modern Treasury. |

### Transaction Line Item

| Action | Method | Description |
| --- | --- | --- |
| [List Transaction Line Items](actions/list-transaction-line-items.md) | GET | Retrieves transaction line items from Modern Treasury. |

### Virtual Account

| Action | Method | Description |
| --- | --- | --- |
| [List Virtual Accounts](actions/list-virtual-accounts.md) | GET | Retrieves virtual accounts from Modern Treasury. |

