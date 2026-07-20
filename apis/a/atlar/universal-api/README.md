# <img src="https://images.mindcloud.co/apps/icons/atlar-icon_1776709722540.png" alt="Atlar logo" width="28" height="28"> Atlar: Universal API

Atlar is a treasury management platform API for payments, financial data, bank connections, accounts, transactions, entities, audit logs, forecasts, and regulatory reporting.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/atlar/latest
- **Actions:** 175
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.atlar.com/
- **Vendor API docs:** https://docs.atlar.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (175)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get account](actions/get-account.md) | GET | Retrieves an account from Atlar. |
| [List accounts](actions/list-accounts.md) | GET | Retrieves accounts from Atlar. |
| [Update account](actions/update-account.md) | PUT | Updates an existing account in Atlar. |
| [V1 Create external account](actions/v1-create-external-account.md) | POST | Creates an external account in Atlar v1. |
| [V1 Delete external account](actions/v1-delete-external-account.md) | DELETE | Deletes an existing external account from Atlar v1. |
| [V1 Modify account](actions/v1-modify-account.md) | PUT | Updates an existing account in Atlar v1. |
| [V1 Query accounts](actions/v1-query-accounts.md) | GET | Retrieves accounts from Atlar v1. |
| [V1 Query external accounts](actions/v1-query-external-accounts.md) | GET | Retrieves external accounts from Atlar v1. |
| [V1 Read account](actions/v1-read-account.md) | GET | Retrieves an account from Atlar v1. |
| [V1 Read external account](actions/v1-read-external-account.md) | GET | Retrieves an external account from Atlar v1. |
| [V1 Update external account](actions/v1-update-external-account.md) | PUT | Updates an existing external account in Atlar v1. |

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create facility activity](actions/create-facility-activity.md) | POST | Creates a facility activity in Atlar. |
| [Create loan activity](actions/create-loan-activity.md) | POST | Creates a loan activity in Atlar. |
| [Delete facility activity](actions/delete-facility-activity.md) | DELETE | Deletes an existing facility activity from Atlar. |
| [Delete loan activity](actions/delete-loan-activity.md) | DELETE | Deletes an existing loan activity from Atlar. |
| [Get facility activity](actions/get-facility-activity.md) | GET | Retrieves a facility activity from Atlar. |
| [Get holding activity](actions/get-holding-activity.md) | GET | Retrieves a holding activity from Atlar. |
| [Get loan activity](actions/get-loan-activity.md) | GET | Retrieves a loan activity from Atlar. |
| [List facility activities](actions/list-facility-activities.md) | GET | Retrieves facility activities from Atlar. |
| [List holding activity](actions/list-holding-activity.md) | GET | Retrieves holding activity from Atlar. |
| [List loan activities](actions/list-loan-activities.md) | GET | Retrieves loan activities from Atlar. |
| [Update facility activity](actions/update-facility-activity.md) | PUT | Updates an existing facility activity in Atlar. |
| [Update loan activity](actions/update-loan-activity.md) | PUT | Updates an existing loan activity in Atlar. |

### Approval

| Action | Method | Description |
| --- | --- | --- |
| [V1 Approve Credit Transfer](actions/v1-approve-credit-transfer.md) | PUT | Approves a credit transfer in Atlar v1. |
| [V1 Reject Credit Transfer](actions/v1-reject-credit-transfer.md) | DELETE | Rejects a credit transfer in Atlar v1. |
| [V1 Reject Direct Debit](actions/v1-reject-direct-debit.md) | DELETE | Rejects a direct debit in Atlar v1. |

### Audit Log Entry

| Action | Method | Description |
| --- | --- | --- |
| [List audit log entries](actions/list-audit-log-entries.md) | GET | Retrieves audit log entries from Atlar. |

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [List balances](actions/list-balances.md) | GET | Retrieves balances from Atlar. |
| [List facility balances](actions/list-facility-balances.md) | GET | Retrieves facility balances from Atlar. |
| [List loan balances](actions/list-loan-balances.md) | GET | Retrieves loan balances from Atlar. |

### Bank Statement

| Action | Method | Description |
| --- | --- | --- |
| [List bank statements](actions/list-bank-statements.md) | GET | Retrieves bank statements from Atlar. |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [List connections](actions/list-connections.md) | GET | Retrieves connections from Atlar. |

### Content

| Action | Method | Description |
| --- | --- | --- |
| [Get bank statement content](actions/get-bank-statement-content.md) | GET | Retrieves bank statement content from Atlar. |
| [Get report content](actions/get-report-content.md) | GET | Retrieves report content from Atlar. |

### Counterparty

| Action | Method | Description |
| --- | --- | --- |
| [Create counterparty](actions/create-counterparty.md) | POST | Creates a counterparty in Atlar. |
| [Delete counterparty](actions/delete-counterparty.md) | DELETE | Deletes an existing counterparty from Atlar. |
| [Get counterparty](actions/get-counterparty.md) | GET | Retrieves a counterparty from Atlar. |
| [Get counterparty by external ID](actions/get-counterparty-by-external-id.md) | GET | Retrieves a counterparty from Atlar by external ID. |
| [List counterparties](actions/list-counterparties.md) | GET | Retrieves counterparties from Atlar. |
| [Update counterparty](actions/update-counterparty.md) | PUT | Updates an existing counterparty in Atlar. |
| [V1 Create counterparty](actions/v1-create-counterparty.md) | POST | Creates a counterparty in Atlar v1. |
| [V1 Delete counterparty](actions/v1-delete-counterparty.md) | DELETE | Deletes an existing counterparty from Atlar v1. |
| [V1 Query counterparties](actions/v1-query-counterparties.md) | GET | Retrieves counterparties from Atlar v1. |
| [V1 Read counterparty](actions/v1-read-counterparty.md) | GET | Retrieves a counterparty from Atlar v1. |
| [V1 Update counterparty](actions/v1-update-counterparty.md) | PUT | Updates an existing counterparty in Atlar v1. |

### Credit

| Action | Method | Description |
| --- | --- | --- |
| [V1 Read credit transfer by its externalId](actions/v1-read-credit-transfer-by-its-externalid.md) | GET | Retrieves a credit transfer by its external ID from Atlar v1. |
| [V1BETA Read credit transfer by its externalId](actions/v1beta-read-credit-transfer-by-its-externalid.md) | GET | Retrieves a credit transfer by its external ID from Atlar v1beta. |

### Credit Transfer

| Action | Method | Description |
| --- | --- | --- |
| [Approve credit transfer](actions/approve-credit-transfer.md) | POST | Approves a credit transfer in Atlar. |
| [Create credit transfer](actions/create-credit-transfer.md) | POST | Creates a credit transfer in Atlar. |
| [Get credit transfer](actions/get-credit-transfer.md) | GET | Retrieves a credit transfer from Atlar. |
| [Get credit transfer by external ID](actions/get-credit-transfer-by-external-id.md) | GET | Retrieves a credit transfer from Atlar by external ID. |
| [List credit transfers](actions/list-credit-transfers.md) | GET | Retrieves credit transfers from Atlar. |
| [Reject credit transfer](actions/reject-credit-transfer.md) | POST | Rejects a credit transfer in Atlar. |
| [Update credit transfer](actions/update-credit-transfer.md) | PUT | Updates an existing credit transfer in Atlar. |

### Credit Transfer Batche

| Action | Method | Description |
| --- | --- | --- |
| [Approve credit transfer batch](actions/approve-credit-transfer-batch.md) | POST | Approves a credit transfer batch in Atlar. |
| [Create credit transfer batch](actions/create-credit-transfer-batch.md) | POST | Creates a credit transfer batch in Atlar. |
| [Get credit transfer batch](actions/get-credit-transfer-batch.md) | GET | Retrieves a credit transfer batch from Atlar. |
| [List credit transfer batches](actions/list-credit-transfer-batches.md) | GET | Retrieves credit transfer batches from Atlar. |
| [Reject credit transfer batch](actions/reject-credit-transfer-batch.md) | POST | Rejects a credit transfer batch in Atlar. |

### Debit

| Action | Method | Description |
| --- | --- | --- |
| [V1 Create Direct Debit](actions/v1-create-direct-debit.md) | POST | Creates a direct debit in Atlar v1. |
| [V1 Query Direct Debits](actions/v1-query-direct-debits.md) | GET | Retrieves direct debits from Atlar v1. |
| [V1 Read Direct Debit](actions/v1-read-direct-debit.md) | GET | Retrieves a direct debit from Atlar v1. |

### Direct

| Action | Method | Description |
| --- | --- | --- |
| [V1 Read Direct Debit by its externalId](actions/v1-read-direct-debit-by-its-externalid.md) | GET | Retrieves a direct debit by its external ID from Atlar v1. |
| [V1BETA Read Direct Debit by its externalId](actions/v1beta-read-direct-debit-by-its-externalid.md) | GET | Retrieves a direct debit by its external ID from Atlar v1beta. |

### Direct Debit

| Action | Method | Description |
| --- | --- | --- |
| [Approve direct debit](actions/approve-direct-debit.md) | POST | Approves a direct debit in Atlar. |
| [Create direct debit](actions/create-direct-debit.md) | POST | Creates a direct debit in Atlar. |
| [Get direct debit](actions/get-direct-debit.md) | GET | Retrieves a direct debit from Atlar. |
| [Get direct debit by external ID](actions/get-direct-debit-by-external-id.md) | GET | Retrieves a direct debit from Atlar by external ID. |
| [List direct debits](actions/list-direct-debits.md) | GET | Retrieves direct debits from Atlar. |
| [Reject direct debit](actions/reject-direct-debit.md) | POST | Rejects a direct debit in Atlar. |

### Direct Debit Batche

| Action | Method | Description |
| --- | --- | --- |
| [Approve direct debit batch](actions/approve-direct-debit-batch.md) | POST | Approves a direct debit batch in Atlar. |
| [Create direct debit batch](actions/create-direct-debit-batch.md) | POST | Creates a direct debit batch in Atlar. |
| [Get direct debit batch](actions/get-direct-debit-batch.md) | GET | Retrieves a direct debit batch from Atlar. |
| [List direct debit batches](actions/list-direct-debit-batches.md) | GET | Retrieves direct debit batches from Atlar. |
| [Reject direct debit batch](actions/reject-direct-debit-batch.md) | POST | Rejects a direct debit batch in Atlar. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create document](actions/create-document.md) | POST | Creates a document in Atlar. |
| [Delete document](actions/delete-document.md) | DELETE | Deletes an existing document from Atlar. |
| [Get document](actions/get-document.md) | GET | Retrieves a document from Atlar. |
| [List documents](actions/list-documents.md) | GET | Retrieves documents from Atlar. |
| [Update document](actions/update-document.md) | PUT | Updates an existing document in Atlar. |

### End Of Day Summary

| Action | Method | Description |
| --- | --- | --- |
| [List end-of-day summaries](actions/list-end-of-day-summaries.md) | GET | Retrieves end-of-day summaries from Atlar. |

### Entity

| Action | Method | Description |
| --- | --- | --- |
| [Create entity](actions/create-entity.md) | POST | Creates an entity in Atlar. |
| [Delete entity](actions/delete-entity.md) | DELETE | Deletes an existing entity from Atlar. |
| [Get entity](actions/get-entity.md) | GET | Retrieves an entity from Atlar. |
| [List entities](actions/list-entities.md) | GET | Retrieves entities from Atlar. |
| [Update entity](actions/update-entity.md) | PUT | Updates an existing entity in Atlar. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List counterparty events](actions/list-counterparty-events.md) | GET | Retrieves counterparty events from Atlar. |
| [List credit transfer events](actions/list-credit-transfer-events.md) | GET | Retrieves credit transfer events from Atlar. |
| [List direct debit events](actions/list-direct-debit-events.md) | GET | Retrieves direct debit events from Atlar. |
| [List forecasted transaction events](actions/list-forecasted-transaction-events.md) | GET | Retrieves forecasted transaction events from Atlar. |
| [List mandate events](actions/list-mandate-events.md) | GET | Retrieves mandate events from Atlar. |
| [List pending transaction events](actions/list-pending-transaction-events.md) | GET | Retrieves pending transaction events from Atlar. |
| [List transaction events](actions/list-transaction-events.md) | GET | Retrieves transaction events from Atlar. |
| [V1 Query Counterparty events](actions/v1-query-counterparty-events.md) | GET | Retrieves counterparty events from Atlar v1. |
| [V1 Query Credit Transfer events](actions/v1-query-credit-transfer-events.md) | GET | Retrieves credit transfer events from Atlar v1. |
| [V1 Query Direct Debit events](actions/v1-query-direct-debit-events.md) | GET | Retrieves direct debit events from Atlar v1. |
| [V1 Query Expected Transaction events](actions/v1-query-expected-transaction-events.md) | GET | Retrieves expected transaction events from Atlar v1. |
| [V1 Query Mandate events](actions/v1-query-mandate-events.md) | GET | Retrieves mandate events from Atlar v1. |
| [V1 Query Transaction events](actions/v1-query-transaction-events.md) | GET | Retrieves transaction events from Atlar v1. |

### External

| Action | Method | Description |
| --- | --- | --- |
| [V1 Read external account by its externalId](actions/v1-read-external-account-by-its-externalid.md) | GET | Retrieves an external account by its external ID from Atlar v1. |
| [V1BETA Read external account by its externalId](actions/v1beta-read-external-account-by-its-externalid.md) | GET | Retrieves an external account by its external ID from Atlar v1beta. |

### External Account

| Action | Method | Description |
| --- | --- | --- |
| [Create external account](actions/create-external-account.md) | POST | Creates an external account in Atlar. |
| [Delete external account](actions/delete-external-account.md) | DELETE | Deletes an existing external account from Atlar. |
| [Get external account](actions/get-external-account.md) | GET | Retrieves an external account from Atlar. |
| [Get external account by external ID](actions/get-external-account-by-external-id.md) | GET | Retrieves an external account from Atlar by external ID. |
| [List external accounts](actions/list-external-accounts.md) | GET | Retrieves external accounts from Atlar. |
| [Update external account](actions/update-external-account.md) | PUT | Updates an existing external account in Atlar. |

### Facility

| Action | Method | Description |
| --- | --- | --- |
| [Create facility](actions/create-facility.md) | POST | Creates a facility in Atlar. |
| [Delete facility](actions/delete-facility.md) | DELETE | Deletes an existing facility from Atlar. |
| [Get facility](actions/get-facility.md) | GET | Retrieves a facility from Atlar. |
| [List facilities](actions/list-facilities.md) | GET | Retrieves facilities from Atlar. |
| [Update facility](actions/update-facility.md) | PUT | Updates an existing facility in Atlar. |

### Forecasted Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Create forecasted transaction](actions/create-forecasted-transaction.md) | POST | Creates a forecasted transaction in Atlar. |
| [Delete forecasted transaction](actions/delete-forecasted-transaction.md) | DELETE | Deletes an existing forecasted transaction from Atlar. |
| [Get forecasted transaction](actions/get-forecasted-transaction.md) | GET | Retrieves a forecasted transaction from Atlar. |
| [List forecasted transactions](actions/list-forecasted-transactions.md) | GET | Retrieves forecasted transactions from Atlar. |
| [Update forecasted transaction](actions/update-forecasted-transaction.md) | PUT | Updates an existing forecasted transaction in Atlar. |

### Holding

| Action | Method | Description |
| --- | --- | --- |
| [Get holding](actions/get-holding.md) | GET | Retrieves a holding from Atlar. |
| [List holdings](actions/list-holdings.md) | GET | Retrieves holdings from Atlar. |

### Idempotency Test

| Action | Method | Description |
| --- | --- | --- |
| [V1 Test idempotency](actions/v1-test-idempotency.md) | POST | Tests idempotency in Atlar v1. |

### Key

| Action | Method | Description |
| --- | --- | --- |
| [V1 Create webhook signing key](actions/v1-create-webhook-signing-key.md) | POST | Creates a webhook signing key in Atlar v1. |
| [V1 Delete webhook key](actions/v1-delete-webhook-key.md) | DELETE | Deletes an existing webhook key from Atlar v1. |

### Loan

| Action | Method | Description |
| --- | --- | --- |
| [Create loan](actions/create-loan.md) | POST | Creates a loan in Atlar. |
| [Delete loan](actions/delete-loan.md) | DELETE | Deletes an existing loan from Atlar. |
| [Get loan](actions/get-loan.md) | GET | Retrieves a loan from Atlar. |
| [List loans](actions/list-loans.md) | GET | Retrieves loans from Atlar. |
| [Update loan](actions/update-loan.md) | PUT | Updates an existing loan in Atlar. |

### Mandate

| Action | Method | Description |
| --- | --- | --- |
| [Cancel mandate](actions/cancel-mandate.md) | DELETE | Cancels a mandate in Atlar. |
| [Create mandate](actions/create-mandate.md) | POST | Creates a mandate in Atlar. |
| [Get mandate](actions/get-mandate.md) | GET | Retrieves a mandate from Atlar. |
| [Get mandate by external ID](actions/get-mandate-by-external-id.md) | GET | Retrieves a mandate from Atlar by external ID. |
| [List mandates](actions/list-mandates.md) | GET | Retrieves mandates from Atlar. |
| [V1 Cancel Mandate](actions/v1-cancel-mandate.md) | POST | Cancels a mandate in Atlar v1. |
| [V1 Create Mandate](actions/v1-create-mandate.md) | POST | Creates a mandate in Atlar v1. |
| [V1 Query Mandates](actions/v1-query-mandates.md) | GET | Retrieves mandates from Atlar v1. |
| [V1 Read Mandate](actions/v1-read-mandate.md) | GET | Retrieves a mandate from Atlar v1. |

### Party

| Action | Method | Description |
| --- | --- | --- |
| [V1BETA Query Third Parties](actions/v1beta-query-third-parties.md) | GET | Retrieves third parties from Atlar v1beta. |
| [V1BETA Read third party](actions/v1beta-read-third-party.md) | GET | Retrieves a third party from Atlar v1beta. |

### Pending Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get pending transaction](actions/get-pending-transaction.md) | GET | Retrieves a pending transaction from Atlar. |
| [List pending transactions](actions/list-pending-transactions.md) | GET | Retrieves pending transactions from Atlar. |
| [Update pending transaction](actions/update-pending-transaction.md) | PUT | Updates an existing pending transaction in Atlar. |

### Portfolio

| Action | Method | Description |
| --- | --- | --- |
| [Get portfolio](actions/get-portfolio.md) | GET | Retrieves a portfolio from Atlar. |
| [List portfolios](actions/list-portfolios.md) | GET | Retrieves portfolios from Atlar. |

### Position

| Action | Method | Description |
| --- | --- | --- |
| [List positions](actions/list-positions.md) | GET | Retrieves positions from Atlar. |

### Regulatory Reporting Code

| Action | Method | Description |
| --- | --- | --- |
| [List regulatory reporting codes](actions/list-regulatory-reporting-codes.md) | GET | Retrieves regulatory reporting codes from Atlar. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [List connection reports](actions/list-connection-reports.md) | GET | Retrieves connection reports from Atlar. |

### Result

| Action | Method | Description |
| --- | --- | --- |
| [List credit transfer batch results](actions/list-credit-transfer-batch-results.md) | GET | Retrieves credit transfer batch results from Atlar. |
| [List direct debit batch results](actions/list-direct-debit-batch-results.md) | GET | Retrieves direct debit batch results from Atlar. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get transaction](actions/get-transaction.md) | GET | Retrieves a transaction from Atlar. |
| [List transactions](actions/list-transactions.md) | GET | Retrieves transactions from Atlar. |
| [Update transaction](actions/update-transaction.md) | PUT | Updates an existing transaction in Atlar. |
| [V1 Create Expected Transaction](actions/v1-create-expected-transaction.md) | POST | Creates an expected transaction in Atlar v1. |
| [V1 Create testbank transaction](actions/v1-create-testbank-transaction.md) | POST | Creates a testbank transaction in Atlar v1. |
| [V1 Query Expected Transactions](actions/v1-query-expected-transactions.md) | GET | Retrieves expected transactions from Atlar v1. |
| [V1 Query transactions](actions/v1-query-transactions.md) | GET | Retrieves transactions from Atlar v1. |
| [V1 Read Expected Transaction](actions/v1-read-expected-transaction.md) | GET | Retrieves an expected transaction from Atlar v1. |
| [V1 Read transaction](actions/v1-read-transaction.md) | GET | Retrieves a transaction from Atlar v1. |
| [V1BETA Archive Expected Transaction](actions/v1beta-archive-expected-transaction.md) | POST | Archives an expected transaction in Atlar v1beta. |
| [V1BETA Reconcile Expected Transaction](actions/v1beta-reconcile-expected-transaction.md) | POST | Reconciles an expected transaction in Atlar v1beta. |
| [V1BETA Unarchive Expected Transaction](actions/v1beta-unarchive-expected-transaction.md) | POST | Unarchives an expected transaction in Atlar v1beta. |
| [V1BETA Unreconcile Expected Transaction](actions/v1beta-unreconcile-expected-transaction.md) | POST | Unreconciles an expected transaction in Atlar v1beta. |

### Transfer

| Action | Method | Description |
| --- | --- | --- |
| [V1 Create Credit Transfer](actions/v1-create-credit-transfer.md) | POST | Creates a credit transfer in Atlar v1. |
| [V1 Query Credit Transfers](actions/v1-query-credit-transfers.md) | GET | Retrieves credit transfers from Atlar v1. |
| [V1 Read Credit Transfer](actions/v1-read-credit-transfer.md) | GET | Retrieves a credit transfer from Atlar v1. |

### V1

| Action | Method | Description |
| --- | --- | --- |
| [V1 Read counterparty by its externalId](actions/v1-read-counterparty-by-its-externalid.md) | GET | Retrieves a counterparty by its external ID from Atlar v1. |
| [V1 Read Mandate by its externalId](actions/v1-read-mandate-by-its-externalid.md) | GET | Retrieves a mandate by its external ID from Atlar v1. |

### V1beta

| Action | Method | Description |
| --- | --- | --- |
| [V1BETA Read counterparty by its externalId](actions/v1beta-read-counterparty-by-its-externalid.md) | GET | Retrieves a counterparty by its external ID from Atlar v1beta. |
| [V1BETA Read Mandate by its externalId](actions/v1beta-read-mandate-by-its-externalid.md) | GET | Retrieves a mandate by its external ID from Atlar v1beta. |

### V2beta

| Action | Method | Description |
| --- | --- | --- |
| [Get documents](actions/get-documents.md) | GET | Retrieves documents from Atlar by ID. |
| [Preview direct debits](actions/preview-direct-debits.md) | POST | Previews direct debits in Atlar. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [V1 Create webhook](actions/v1-create-webhook.md) | POST | Creates a webhook in Atlar v1. |
| [V1 Delete webhook](actions/v1-delete-webhook.md) | DELETE | Deletes an existing webhook from Atlar v1. |
| [V1 Query webhooks](actions/v1-query-webhooks.md) | GET | Retrieves webhooks from Atlar v1. |
| [V1 Read webhook](actions/v1-read-webhook.md) | GET | Retrieves a webhook from Atlar v1. |
| [V1 Update webhook](actions/v1-update-webhook.md) | PUT | Updates an existing webhook in Atlar v1. |

