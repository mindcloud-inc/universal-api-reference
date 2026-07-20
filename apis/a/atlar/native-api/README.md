# Atlar: Native API Reference

A consolidated summary of Atlar's API configuration and 175 documented operations, with links to official documentation.

- **Official docs:** https://docs.atlar.com/reference
- **OpenAPI specification:** https://cdn.atlar.com/api/atlar.oas31.yaml
- **API base URL:** `https://api.atlar.com`

## Authentication

### Basic Auth

Authenticate with an Atlar programmatic access user access key and secret using HTTP Basic authentication.

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

[Official authentication documentation](https://docs.atlar.com/docs/accessing-the-api)

## API conventions

The next-page cursor is read from `nextToken`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–500). Use `token` in the query string as the pagination cursor; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts.

## Endpoints (175 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Approve credit transfer](actions/approve-credit-transfer.md) | `POST /payments/v2/credit-transfers/{id}:approve` | [docs](https://docs.atlar.com/reference/post-payments-v2-credit-transfers-id-approve) |
| [Approve credit transfer batch](actions/approve-credit-transfer-batch.md) | `POST /payments/v2/credit-transfer-batches/{id}:approve` | [docs](https://docs.atlar.com/reference/post-payments-v2-credit-transfer-batches-id-approve) |
| [Approve direct debit](actions/approve-direct-debit.md) | `POST /payments/v2/direct-debits/{id}:approve` | [docs](https://docs.atlar.com/reference/post-payments-v2-direct-debits-id-approve) |
| [Approve direct debit batch](actions/approve-direct-debit-batch.md) | `POST /payments/v2beta/direct-debit-batches/{id}:approve` | [docs](https://docs.atlar.com/reference/post-payments-v2beta-direct-debit-batches-id-approve) |
| [Cancel mandate](actions/cancel-mandate.md) | `POST /payments/v2/mandates/{id}:cancel` | [docs](https://docs.atlar.com/reference/post-payments-v2-mandates-id-cancel) |
| [Create counterparty](actions/create-counterparty.md) | `POST /payments/v2/counterparties` | [docs](https://docs.atlar.com/reference/post-payments-v2-counterparties) |
| [Create credit transfer](actions/create-credit-transfer.md) | `POST /payments/v2/credit-transfers` | [docs](https://docs.atlar.com/reference/post-payments-v2-credit-transfers) |
| [Create credit transfer batch](actions/create-credit-transfer-batch.md) | `POST /payments/v2beta/credit-transfer-batches` | [docs](https://docs.atlar.com/reference/post-payments-v2beta-credit-transfer-batches) |
| [Create direct debit](actions/create-direct-debit.md) | `POST /payments/v2/direct-debits` | [docs](https://docs.atlar.com/reference/post-payments-v2-direct-debits) |
| [Create direct debit batch](actions/create-direct-debit-batch.md) | `POST /payments/v2beta/direct-debit-batches` | [docs](https://docs.atlar.com/reference/post-payments-v2beta-direct-debit-batches) |
| [Create document](actions/create-document.md) | `POST /accounting/v2beta/documents` | [docs](https://docs.atlar.com/reference/post-accounting-v2beta-documents) |
| [Create entity](actions/create-entity.md) | `POST /financial-data/v2/entities` | [docs](https://docs.atlar.com/reference/post-financial-data-v2-entities) |
| [Create external account](actions/create-external-account.md) | `POST /payments/v2/external-accounts` | [docs](https://docs.atlar.com/reference/post-payments-v2-external-accounts) |
| [Create facility](actions/create-facility.md) | `POST /financial-data/v2beta/facilities` | [docs](https://docs.atlar.com/reference/post-financial-data-v2beta-facilities) |
| [Create facility activity](actions/create-facility-activity.md) | `POST /financial-data/v2beta/facilities/{id}/activities` | [docs](https://docs.atlar.com/reference/post-financial-data-v2beta-facilities-id-activities) |
| [Create forecasted transaction](actions/create-forecasted-transaction.md) | `POST /analytics/v2beta/forecasted-transactions` | [docs](https://docs.atlar.com/reference/post-analytics-v2beta-forecasted-transactions) |
| [Create loan](actions/create-loan.md) | `POST /financial-data/v2beta/loans` | [docs](https://docs.atlar.com/reference/post-financial-data-v2beta-loans) |
| [Create loan activity](actions/create-loan-activity.md) | `POST /financial-data/v2beta/loans/{loanId}/activities` | [docs](https://docs.atlar.com/reference/post-financial-data-v2beta-loans-loanid-activities) |
| [Create mandate](actions/create-mandate.md) | `POST /payments/v2/mandates` | [docs](https://docs.atlar.com/reference/post-payments-v2-mandates) |
| [Delete counterparty](actions/delete-counterparty.md) | `DELETE /payments/v2/counterparties/{id}` | [docs](https://docs.atlar.com/reference/delete-payments-v2-counterparties-id) |
| [Delete document](actions/delete-document.md) | `DELETE /accounting/v2beta/documents/{id}` | [docs](https://docs.atlar.com/reference/delete-accounting-v2beta-documents-id) |
| [Delete entity](actions/delete-entity.md) | `DELETE /financial-data/v2/entities/{id}` | [docs](https://docs.atlar.com/reference/delete-financial-data-v2-entities-id) |
| [Delete external account](actions/delete-external-account.md) | `DELETE /payments/v2/external-accounts/{id}` | [docs](https://docs.atlar.com/reference/delete-payments-v2-external-accounts-id) |
| [Delete facility](actions/delete-facility.md) | `DELETE /financial-data/v2beta/facilities/{id}` | [docs](https://docs.atlar.com/reference/delete-financial-data-v2beta-facilities-id) |
| [Delete facility activity](actions/delete-facility-activity.md) | `DELETE /financial-data/v2beta/facilities/{id}/activities/{activityId}` | [docs](https://docs.atlar.com/reference/delete-financial-data-v2beta-facilities-id-activities-activityid) |
| [Delete forecasted transaction](actions/delete-forecasted-transaction.md) | `DELETE /analytics/v2beta/forecasted-transactions/{id}` | [docs](https://docs.atlar.com/reference/delete-analytics-v2beta-forecasted-transactions-id) |
| [Delete loan](actions/delete-loan.md) | `DELETE /financial-data/v2beta/loans/{id}` | [docs](https://docs.atlar.com/reference/delete-financial-data-v2beta-loans-id) |
| [Delete loan activity](actions/delete-loan-activity.md) | `DELETE /financial-data/v2beta/loans/{loanId}/activities/{id}` | [docs](https://docs.atlar.com/reference/delete-financial-data-v2beta-loans-loanid-activities-id) |
| [Get account](actions/get-account.md) | `GET /financial-data/v2/accounts/{id}` | [docs](https://docs.atlar.com/reference/get-financial-data-v2-accounts-id) |
| [Get bank statement content](actions/get-bank-statement-content.md) | `GET /connectivity/v2beta/connections/{cid}/reports/{rid}/bank-statements/{id}/content` | [docs](https://docs.atlar.com/reference/get-connectivity-v2beta-connections-cid-reports-rid-bank-statements-id-content) |
| [Get counterparty](actions/get-counterparty.md) | `GET /payments/v2/counterparties/{id}` | [docs](https://docs.atlar.com/reference/get-payments-v2-counterparties-id) |
| [Get counterparty by external ID](actions/get-counterparty-by-external-id.md) | `GET /payments/v2/counterparties/external:{externalId}` | [docs](https://docs.atlar.com/docs/migrate-from-v1-to-v2) |
| [Get credit transfer](actions/get-credit-transfer.md) | `GET /payments/v2/credit-transfers/{id}` | [docs](https://docs.atlar.com/reference/get-payments-v2-credit-transfers-id) |
| [Get credit transfer batch](actions/get-credit-transfer-batch.md) | `GET /payments/v2beta/credit-transfer-batches/{id}` | [docs](https://docs.atlar.com/reference/get-payments-v2beta-credit-transfer-batches-id) |
| [Get credit transfer by external ID](actions/get-credit-transfer-by-external-id.md) | `GET /payments/v2/credit-transfers/external:{externalId}` | [docs](https://docs.atlar.com/docs/migrate-from-v1-to-v2) |
| [Get direct debit](actions/get-direct-debit.md) | `GET /payments/v2/direct-debits/{id}` | [docs](https://docs.atlar.com/reference/get-payments-v2-direct-debits-id) |
| [Get direct debit batch](actions/get-direct-debit-batch.md) | `GET /payments/v2beta/direct-debit-batches/{id}` | [docs](https://docs.atlar.com/reference/get-payments-v2beta-direct-debit-batches-id) |
| [Get direct debit by external ID](actions/get-direct-debit-by-external-id.md) | `GET /payments/v2/direct-debits/external:{externalId}` | [docs](https://docs.atlar.com/docs/migrate-from-v1-to-v2) |
| [Get document](actions/get-document.md) | `GET /accounting/v2beta/documents/{id}` | [docs](https://docs.atlar.com/reference/get-accounting-v2beta-documents-id) |
| [Get documents](actions/get-documents.md) | `GET /accounting/v2beta/documents:batch` | [docs](https://docs.atlar.com/reference/get-accounting-v2beta-documents-batch) |
| [Get entity](actions/get-entity.md) | `GET /financial-data/v2/entities/{id}` | [docs](https://docs.atlar.com/reference/get-financial-data-v2-entities-id) |
| [Get external account](actions/get-external-account.md) | `GET /payments/v2/external-accounts/{id}` | [docs](https://docs.atlar.com/reference/get-payments-v2-external-accounts-id) |
| [Get external account by external ID](actions/get-external-account-by-external-id.md) | `GET /payments/v2/external-accounts/external:{externalId}` | [docs](https://docs.atlar.com/docs/migrate-from-v1-to-v2) |
| [Get facility](actions/get-facility.md) | `GET /financial-data/v2beta/facilities/{id}` | [docs](https://docs.atlar.com/reference/get-financial-data-v2beta-facilities-id) |
| [Get facility activity](actions/get-facility-activity.md) | `GET /financial-data/v2beta/facilities/{id}/activities/{activityId}` | [docs](https://docs.atlar.com/reference/get-financial-data-v2beta-facilities-id-activities-activityid) |
| [Get forecasted transaction](actions/get-forecasted-transaction.md) | `GET /analytics/v2beta/forecasted-transactions/{id}` | [docs](https://docs.atlar.com/reference/get-analytics-v2beta-forecasted-transactions-id) |
| [Get holding](actions/get-holding.md) | `GET /financial-data/v2beta/portfolios/{pid}/holdings/{id}` | [docs](https://docs.atlar.com/reference/get-financial-data-v2beta-portfolios-pid-holdings-id) |
| [Get holding activity](actions/get-holding-activity.md) | `GET /financial-data/v2beta/portfolios/{pid}/holdings/{hid}/activities/{id}` | [docs](https://docs.atlar.com/reference/get-financial-data-v2beta-portfolios-pid-holdings-hid-activities-id) |
| [Get loan](actions/get-loan.md) | `GET /financial-data/v2beta/loans/{id}` | [docs](https://docs.atlar.com/reference/get-financial-data-v2beta-loans-id) |
| [Get loan activity](actions/get-loan-activity.md) | `GET /financial-data/v2beta/loans/{loanId}/activities/{id}` | [docs](https://docs.atlar.com/reference/get-financial-data-v2beta-loans-loanid-activities-id) |
| [Get mandate](actions/get-mandate.md) | `GET /payments/v2/mandates/{id}` | [docs](https://docs.atlar.com/reference/get-payments-v2-mandates-id) |
| [Get mandate by external ID](actions/get-mandate-by-external-id.md) | `GET /payments/v2/mandates/external:{externalId}` | [docs](https://docs.atlar.com/docs/migrate-from-v1-to-v2) |
| [Get pending transaction](actions/get-pending-transaction.md) | `GET /financial-data/v2/pending-transactions/{id}` | [docs](https://docs.atlar.com/reference/get-financial-data-v2-pending-transactions-id) |
| [Get portfolio](actions/get-portfolio.md) | `GET /financial-data/v2beta/portfolios/{id}` | [docs](https://docs.atlar.com/reference/get-financial-data-v2beta-portfolios-id) |
| [Get report content](actions/get-report-content.md) | `GET /connectivity/v2beta/connections/{cid}/reports/{id}/content` | [docs](https://docs.atlar.com/reference/get-connectivity-v2beta-connections-cid-reports-id-content) |
| [Get transaction](actions/get-transaction.md) | `GET /financial-data/v2/transactions/{id}` | [docs](https://docs.atlar.com/reference/get-financial-data-v2-transactions-id) |
| [List accounts](actions/list-accounts.md) | `GET /financial-data/v2/accounts` | [docs](https://docs.atlar.com/reference/get-financial-data-v2-accounts) |
| [List audit log entries](actions/list-audit-log-entries.md) | `GET /iam/v2beta/audit-log-entries` | [docs](https://docs.atlar.com/reference/get-iam-v2beta-audit-log-entries) |
| [List balances](actions/list-balances.md) | `GET /financial-data/v2/accounts/{id}/balances` | [docs](https://docs.atlar.com/reference/get-financial-data-v2-accounts-id-balances) |
| [List bank statements](actions/list-bank-statements.md) | `GET /connectivity/v2beta/connections/{cid}/reports/{id}/bank-statements` | [docs](https://docs.atlar.com/reference/get-connectivity-v2beta-connections-cid-reports-id-bank-statements) |
| [List connection reports](actions/list-connection-reports.md) | `GET /connectivity/v2beta/connections/{cid}/reports` | [docs](https://docs.atlar.com/reference/get-connectivity-v2beta-connections-cid-reports) |
| [List connections](actions/list-connections.md) | `GET /connectivity/v2beta/connections` | [docs](https://docs.atlar.com/reference/get-connectivity-v2beta-connections) |
| [List counterparties](actions/list-counterparties.md) | `GET /payments/v2/counterparties` | [docs](https://docs.atlar.com/reference/get-payments-v2-counterparties) |
| [List counterparty events](actions/list-counterparty-events.md) | `GET /payments/v2/counterparties/{id}/events` | [docs](https://docs.atlar.com/reference/get-payments-v2-counterparties-id-events) |
| [List credit transfer batch results](actions/list-credit-transfer-batch-results.md) | `GET /payments/v2beta/credit-transfer-batches/{id}/results` | [docs](https://docs.atlar.com/reference/get-payments-v2beta-credit-transfer-batches-id-results) |
| [List credit transfer batches](actions/list-credit-transfer-batches.md) | `GET /payments/v2beta/credit-transfer-batches` | [docs](https://docs.atlar.com/reference/get-payments-v2beta-credit-transfer-batches) |
| [List credit transfer events](actions/list-credit-transfer-events.md) | `GET /payments/v2/credit-transfers/{id}/events` | [docs](https://docs.atlar.com/reference/get-payments-v2-credit-transfers-id-events) |
| [List credit transfers](actions/list-credit-transfers.md) | `GET /payments/v2/credit-transfers` | [docs](https://docs.atlar.com/reference/get-payments-v2-credit-transfers) |
| [List direct debit batch results](actions/list-direct-debit-batch-results.md) | `GET /payments/v2beta/direct-debit-batches/{id}/results` | [docs](https://docs.atlar.com/reference/get-payments-v2beta-direct-debit-batches-id-results) |
| [List direct debit batches](actions/list-direct-debit-batches.md) | `GET /payments/v2beta/direct-debit-batches` | [docs](https://docs.atlar.com/reference/get-payments-v2beta-direct-debit-batches) |
| [List direct debit events](actions/list-direct-debit-events.md) | `GET /payments/v2/direct-debits/{id}/events` | [docs](https://docs.atlar.com/reference/get-payments-v2-direct-debits-id-events) |
| [List direct debits](actions/list-direct-debits.md) | `GET /payments/v2/direct-debits` | [docs](https://docs.atlar.com/reference/get-payments-v2-direct-debits) |
| [List documents](actions/list-documents.md) | `GET /accounting/v2beta/documents` | [docs](https://docs.atlar.com/reference/get-accounting-v2beta-documents) |
| [List end-of-day summaries](actions/list-end-of-day-summaries.md) | `GET /financial-data/v2beta/accounts/{id}/end-of-day-summaries` | [docs](https://docs.atlar.com/reference/get-financial-data-v2beta-accounts-id-end-of-day-summaries) |
| [List entities](actions/list-entities.md) | `GET /financial-data/v2/entities` | [docs](https://docs.atlar.com/reference/get-financial-data-v2-entities) |
| [List external accounts](actions/list-external-accounts.md) | `GET /payments/v2/external-accounts` | [docs](https://docs.atlar.com/reference/get-payments-v2-external-accounts) |
| [List facilities](actions/list-facilities.md) | `GET /financial-data/v2beta/facilities` | [docs](https://docs.atlar.com/reference/get-financial-data-v2beta-facilities) |
| [List facility activities](actions/list-facility-activities.md) | `GET /financial-data/v2beta/facilities/{id}/activities` | [docs](https://docs.atlar.com/reference/get-financial-data-v2beta-facilities-id-activities) |
| [List facility balances](actions/list-facility-balances.md) | `GET /financial-data/v2beta/facilities/{id}/balances` | [docs](https://docs.atlar.com/reference/get-financial-data-v2beta-facilities-id-balances) |
| [List forecasted transaction events](actions/list-forecasted-transaction-events.md) | `GET /analytics/v2beta/forecasted-transactions/{id}/events` | [docs](https://docs.atlar.com/reference/get-analytics-v2beta-forecasted-transactions-id-events) |
| [List forecasted transactions](actions/list-forecasted-transactions.md) | `GET /analytics/v2beta/forecasted-transactions` | [docs](https://docs.atlar.com/reference/get-analytics-v2beta-forecasted-transactions) |
| [List holding activity](actions/list-holding-activity.md) | `GET /financial-data/v2beta/portfolios/{pid}/holdings/{id}/activities` | [docs](https://docs.atlar.com/reference/get-financial-data-v2beta-portfolios-pid-holdings-id-activities) |
| [List holdings](actions/list-holdings.md) | `GET /financial-data/v2beta/portfolios/{id}/holdings` | [docs](https://docs.atlar.com/reference/get-financial-data-v2beta-portfolios-id-holdings) |
| [List loan activities](actions/list-loan-activities.md) | `GET /financial-data/v2beta/loans/{loanId}/activities` | [docs](https://docs.atlar.com/reference/get-financial-data-v2beta-loans-loanid-activities) |
| [List loan balances](actions/list-loan-balances.md) | `GET /financial-data/v2beta/loans/{loanId}/balances` | [docs](https://docs.atlar.com/reference/get-financial-data-v2beta-loans-loanid-balances) |
| [List loans](actions/list-loans.md) | `GET /financial-data/v2beta/loans` | [docs](https://docs.atlar.com/reference/get-financial-data-v2beta-loans) |
| [List mandate events](actions/list-mandate-events.md) | `GET /payments/v2/mandates/{id}/events` | [docs](https://docs.atlar.com/reference/get-payments-v2-mandates-id-events) |
| [List mandates](actions/list-mandates.md) | `GET /payments/v2/mandates` | [docs](https://docs.atlar.com/reference/get-payments-v2-mandates) |
| [List pending transaction events](actions/list-pending-transaction-events.md) | `GET /financial-data/v2/pending-transactions/{id}/events` | [docs](https://docs.atlar.com/reference/get-financial-data-v2-pending-transactions-id-events) |
| [List pending transactions](actions/list-pending-transactions.md) | `GET /financial-data/v2/pending-transactions` | [docs](https://docs.atlar.com/reference/get-financial-data-v2-pending-transactions) |
| [List portfolios](actions/list-portfolios.md) | `GET /financial-data/v2beta/portfolios` | [docs](https://docs.atlar.com/reference/get-financial-data-v2beta-portfolios) |
| [List positions](actions/list-positions.md) | `GET /financial-data/v2beta/portfolios/{pid}/holdings/{id}/positions` | [docs](https://docs.atlar.com/reference/get-financial-data-v2beta-portfolios-pid-holdings-id-positions) |
| [List regulatory reporting codes](actions/list-regulatory-reporting-codes.md) | `GET /payments/v2/regulatory-reporting-codes` | [docs](https://docs.atlar.com/reference/get-payments-v2-regulatory-reporting-codes) |
| [List transaction events](actions/list-transaction-events.md) | `GET /financial-data/v2/transactions/{id}/events` | [docs](https://docs.atlar.com/reference/get-financial-data-v2-transactions-id-events) |
| [List transactions](actions/list-transactions.md) | `GET /financial-data/v2/transactions` | [docs](https://docs.atlar.com/reference/get-financial-data-v2-transactions) |
| [Preview direct debits](actions/preview-direct-debits.md) | `POST /payments/v2beta/direct-debit-batches:preview` | [docs](https://docs.atlar.com/reference/post-payments-v2beta-direct-debit-batches-preview) |
| [Reject credit transfer](actions/reject-credit-transfer.md) | `POST /payments/v2/credit-transfers/{id}:reject` | [docs](https://docs.atlar.com/reference/post-payments-v2-credit-transfers-id-reject) |
| [Reject credit transfer batch](actions/reject-credit-transfer-batch.md) | `POST /payments/v2/credit-transfer-batches/{id}:reject` | [docs](https://docs.atlar.com/reference/post-payments-v2-credit-transfer-batches-id-reject) |
| [Reject direct debit](actions/reject-direct-debit.md) | `POST /payments/v2/direct-debits/{id}:reject` | [docs](https://docs.atlar.com/reference/post-payments-v2-direct-debits-id-reject) |
| [Reject direct debit batch](actions/reject-direct-debit-batch.md) | `POST /payments/v2beta/direct-debit-batches/{id}:reject` | [docs](https://docs.atlar.com/reference/post-payments-v2beta-direct-debit-batches-id-reject) |
| [Update account](actions/update-account.md) | `PATCH /financial-data/v2/accounts/{id}` | [docs](https://docs.atlar.com/reference/patch-financial-data-v2-accounts-id) |
| [Update counterparty](actions/update-counterparty.md) | `PATCH /payments/v2/counterparties/{id}` | [docs](https://docs.atlar.com/reference/patch-payments-v2-counterparties-id) |
| [Update credit transfer](actions/update-credit-transfer.md) | `PATCH /payments/v2/credit-transfers/{id}` | [docs](https://docs.atlar.com/reference/patch-payments-v2-credit-transfers-id) |
| [Update document](actions/update-document.md) | `PATCH /accounting/v2beta/documents/{id}` | [docs](https://docs.atlar.com/reference/patch-accounting-v2beta-documents-id) |
| [Update entity](actions/update-entity.md) | `PATCH /financial-data/v2/entities/{id}` | [docs](https://docs.atlar.com/reference/patch-financial-data-v2-entities-id) |
| [Update external account](actions/update-external-account.md) | `PATCH /payments/v2/external-accounts/{id}` | [docs](https://docs.atlar.com/reference/patch-payments-v2-external-accounts-id) |
| [Update facility](actions/update-facility.md) | `PATCH /financial-data/v2beta/facilities/{id}` | [docs](https://docs.atlar.com/reference/patch-financial-data-v2beta-facilities-id) |
| [Update facility activity](actions/update-facility-activity.md) | `PATCH /financial-data/v2beta/facilities/{id}/activities/{activityId}` | [docs](https://docs.atlar.com/reference/patch-financial-data-v2beta-facilities-id-activities-activityid) |
| [Update forecasted transaction](actions/update-forecasted-transaction.md) | `PATCH /analytics/v2beta/forecasted-transactions/{id}` | [docs](https://docs.atlar.com/reference/patch-analytics-v2beta-forecasted-transactions-id) |
| [Update loan](actions/update-loan.md) | `PATCH /financial-data/v2beta/loans/{id}` | [docs](https://docs.atlar.com/reference/patch-financial-data-v2beta-loans-id) |
| [Update loan activity](actions/update-loan-activity.md) | `PATCH /financial-data/v2beta/loans/{loanId}/activities/{id}` | [docs](https://docs.atlar.com/reference/patch-financial-data-v2beta-loans-loanid-activities-id) |
| [Update pending transaction](actions/update-pending-transaction.md) | `PATCH /financial-data/v2beta/pending-transactions/{id}` | [docs](https://docs.atlar.com/reference/patch-financial-data-v2beta-pending-transactions-id) |
| [Update transaction](actions/update-transaction.md) | `PATCH /financial-data/v2/transactions/{id}` | [docs](https://docs.atlar.com/reference/patch-financial-data-v2-transactions-id) |
| [V1 Approve Credit Transfer](actions/v1-approve-credit-transfer.md) | `PUT /v1/credit-transfers/{id}/approvals/{approvalStepId}` | [docs](https://docs.atlar.com/v1/reference/put_v1-credit-transfers-id-approvals-approvalstepid) |
| [V1 Cancel Mandate](actions/v1-cancel-mandate.md) | `POST /v1/mandates/{id}:cancel` | [docs](https://docs.atlar.com/v1/reference/post_v1-mandates-id-cancel) |
| [V1 Create counterparty](actions/v1-create-counterparty.md) | `POST /v1/counterparties` | [docs](https://docs.atlar.com/v1/reference/post_v1-counterparties) |
| [V1 Create Credit Transfer](actions/v1-create-credit-transfer.md) | `POST /v1/credit-transfers` | [docs](https://docs.atlar.com/v1/reference/post_v1-credit-transfers) |
| [V1 Create Direct Debit](actions/v1-create-direct-debit.md) | `POST /v1/direct-debits` | [docs](https://docs.atlar.com/v1/reference/post_v1-direct-debits) |
| [V1 Create Expected Transaction](actions/v1-create-expected-transaction.md) | `POST /v1/expected-transactions` | [docs](https://docs.atlar.com/v1/reference/post_v1-expected-transactions) |
| [V1 Create external account](actions/v1-create-external-account.md) | `POST /v1/external-accounts` | [docs](https://docs.atlar.com/v1/reference/post_v1-external-accounts) |
| [V1 Create Mandate](actions/v1-create-mandate.md) | `POST /v1/mandates` | [docs](https://docs.atlar.com/v1/reference/post_v1-mandates) |
| [V1 Create testbank transaction](actions/v1-create-testbank-transaction.md) | `POST /v1/testbank/transactions` | [docs](https://docs.atlar.com/v1/reference/createtestbanktransaction) |
| [V1 Create webhook](actions/v1-create-webhook.md) | `POST /v1/webhooks` | [docs](https://docs.atlar.com/v1/reference/post_v1-webhooks) |
| [V1 Create webhook signing key](actions/v1-create-webhook-signing-key.md) | `POST /v1/webhooks/{id}/keys` | [docs](https://docs.atlar.com/v1/reference/post_v1-webhooks-id-keys) |
| [V1 Delete counterparty](actions/v1-delete-counterparty.md) | `DELETE /v1/counterparties/{id}` | [docs](https://docs.atlar.com/v1/reference/delete_v1-counterparties-id) |
| [V1 Delete external account](actions/v1-delete-external-account.md) | `DELETE /v1/external-accounts/{id}` | [docs](https://docs.atlar.com/v1/reference/delete_v1-external-accounts-id) |
| [V1 Delete webhook](actions/v1-delete-webhook.md) | `DELETE /v1/webhooks/{id}` | [docs](https://docs.atlar.com/v1/reference/delete_v1-webhooks-id) |
| [V1 Delete webhook key](actions/v1-delete-webhook-key.md) | `DELETE /v1/webhooks/{id}/keys/{keyId}` | [docs](https://docs.atlar.com/v1/reference/delete_v1-webhooks-id-keys-keyid) |
| [V1 Modify account](actions/v1-modify-account.md) | `PUT /v1/accounts/{id}` | [docs](https://docs.atlar.com/v1/reference/put_v1-accounts-id) |
| [V1 Query accounts](actions/v1-query-accounts.md) | `GET /v1/accounts` | [docs](https://docs.atlar.com/v1/reference/get_v1-accounts) |
| [V1 Query counterparties](actions/v1-query-counterparties.md) | `GET /v1/counterparties` | [docs](https://docs.atlar.com/v1/reference/get_v1-counterparties) |
| [V1 Query Counterparty events](actions/v1-query-counterparty-events.md) | `GET /v1/counterparties/{id}/events` | [docs](https://docs.atlar.com/v1/reference/get_v1-counterparties-id-events) |
| [V1 Query Credit Transfer events](actions/v1-query-credit-transfer-events.md) | `GET /v1/credit-transfers/{id}/events` | [docs](https://docs.atlar.com/v1/reference/get_v1-credit-transfers-id-events) |
| [V1 Query Credit Transfers](actions/v1-query-credit-transfers.md) | `GET /v1/credit-transfers` | [docs](https://docs.atlar.com/v1/reference/get_v1-credit-transfers) |
| [V1 Query Direct Debit events](actions/v1-query-direct-debit-events.md) | `GET /v1/direct-debits/{id}/events` | [docs](https://docs.atlar.com/v1/reference/get_v1-direct-debits-id-events) |
| [V1 Query Direct Debits](actions/v1-query-direct-debits.md) | `GET /v1/direct-debits` | [docs](https://docs.atlar.com/v1/reference/get_v1-direct-debits) |
| [V1 Query Expected Transaction events](actions/v1-query-expected-transaction-events.md) | `GET /v1/expected-transactions/{id}/events` | [docs](https://docs.atlar.com/v1/reference/get_v1-expected-transactions-id-events) |
| [V1 Query Expected Transactions](actions/v1-query-expected-transactions.md) | `GET /v1/expected-transactions` | [docs](https://docs.atlar.com/v1/reference/get_v1-expected-transactions) |
| [V1 Query external accounts](actions/v1-query-external-accounts.md) | `GET /v1/external-accounts` | [docs](https://docs.atlar.com/v1/reference/get_v1-external-accounts) |
| [V1 Query Mandate events](actions/v1-query-mandate-events.md) | `GET /v1/mandates/{id}/events` | [docs](https://docs.atlar.com/v1/reference/get_v1-mandates-id-events) |
| [V1 Query Mandates](actions/v1-query-mandates.md) | `GET /v1/mandates` | [docs](https://docs.atlar.com/v1/reference/get_v1-mandates) |
| [V1 Query Transaction events](actions/v1-query-transaction-events.md) | `GET /v1/transactions/{id}/events` | [docs](https://docs.atlar.com/v1/reference/get_v1-transactions-id-events) |
| [V1 Query transactions](actions/v1-query-transactions.md) | `GET /v1/transactions` | [docs](https://docs.atlar.com/v1/reference/get_v1-transactions) |
| [V1 Query webhooks](actions/v1-query-webhooks.md) | `GET /v1/webhooks` | [docs](https://docs.atlar.com/v1/reference/get_v1-webhooks) |
| [V1 Read account](actions/v1-read-account.md) | `GET /v1/accounts/{id}` | [docs](https://docs.atlar.com/v1/reference/get_v1-accounts-id) |
| [V1 Read counterparty](actions/v1-read-counterparty.md) | `GET /v1/counterparties/{id}` | [docs](https://docs.atlar.com/v1/reference/get_v1-counterparties-id) |
| [V1 Read counterparty by its externalId](actions/v1-read-counterparty-by-its-externalid.md) | `GET /v1/counterparties:getByExternalId/{externalId}` | [docs](https://docs.atlar.com/v1/reference/get_v1-counterparties-getbyexternalid-externalid) |
| [V1 Read Credit Transfer](actions/v1-read-credit-transfer.md) | `GET /v1/credit-transfers/{id}` | [docs](https://docs.atlar.com/v1/reference/get_v1-credit-transfers-id) |
| [V1 Read credit transfer by its externalId](actions/v1-read-credit-transfer-by-its-externalid.md) | `GET /v1/credit-transfers:getByExternalId/{externalId}` | [docs](https://docs.atlar.com/v1/reference/get_v1-credit-transfers-getbyexternalid-externalid) |
| [V1 Read Direct Debit](actions/v1-read-direct-debit.md) | `GET /v1/direct-debits/{id}` | [docs](https://docs.atlar.com/v1/reference/get_v1-direct-debits-id) |
| [V1 Read Direct Debit by its externalId](actions/v1-read-direct-debit-by-its-externalid.md) | `GET /v1/direct-debits:getByExternalId/{externalId}` | [docs](https://docs.atlar.com/v1/reference/get_v1-direct-debits-getbyexternalid-externalid) |
| [V1 Read Expected Transaction](actions/v1-read-expected-transaction.md) | `GET /v1/expected-transactions/{id}` | [docs](https://docs.atlar.com/v1/reference/get_v1-expected-transactions-id) |
| [V1 Read external account](actions/v1-read-external-account.md) | `GET /v1/external-accounts/{id}` | [docs](https://docs.atlar.com/v1/reference/get_v1-external-accounts-id) |
| [V1 Read external account by its externalId](actions/v1-read-external-account-by-its-externalid.md) | `GET /v1/external-accounts:getByExternalId/{externalId}` | [docs](https://docs.atlar.com/v1/reference/get_v1-external-accounts-getbyexternalid-externalid) |
| [V1 Read Mandate](actions/v1-read-mandate.md) | `GET /v1/mandates/{id}` | [docs](https://docs.atlar.com/v1/reference/get_v1-mandates-id) |
| [V1 Read Mandate by its externalId](actions/v1-read-mandate-by-its-externalid.md) | `GET /v1/mandates:getByExternalId/{externalId}` | [docs](https://docs.atlar.com/v1/reference/get_v1-mandates-getbyexternalid-externalid) |
| [V1 Read transaction](actions/v1-read-transaction.md) | `GET /v1/transactions/{id}` | [docs](https://docs.atlar.com/v1/reference/get_v1-transactions-id) |
| [V1 Read webhook](actions/v1-read-webhook.md) | `GET /v1/webhooks/{id}` | [docs](https://docs.atlar.com/v1/reference/get_v1-webhooks-id) |
| [V1 Reject Credit Transfer](actions/v1-reject-credit-transfer.md) | `DELETE /v1/credit-transfers/{id}/approvals` | [docs](https://docs.atlar.com/v1/reference/delete_v1-credit-transfers-id-approvals) |
| [V1 Reject Direct Debit](actions/v1-reject-direct-debit.md) | `DELETE /v1/direct-debits/{id}/approvals` | [docs](https://docs.atlar.com/v1/reference/delete_v1-direct-debits-id-approvals) |
| [V1 Test idempotency](actions/v1-test-idempotency.md) | `POST /v1/idempotency-test` | [docs](https://docs.atlar.com/v1/reference/post_v1-idempotency-test) |
| [V1 Update counterparty](actions/v1-update-counterparty.md) | `PUT /v1/counterparties/{id}` | [docs](https://docs.atlar.com/v1/reference/put_v1-counterparties-id) |
| [V1 Update external account](actions/v1-update-external-account.md) | `PUT /v1/external-accounts/{id}` | [docs](https://docs.atlar.com/v1/reference/put_v1-external-accounts-id) |
| [V1 Update webhook](actions/v1-update-webhook.md) | `PUT /v1/webhooks/{id}` | [docs](https://docs.atlar.com/v1/reference/put_v1-webhooks-id) |
| [V1BETA Archive Expected Transaction](actions/v1beta-archive-expected-transaction.md) | `POST /v1beta/expected-transactions/{id}:archive` | [docs](https://docs.atlar.com/v1/reference/post_v1beta-expected-transactions-id-archive) |
| [V1BETA Query Third Parties](actions/v1beta-query-third-parties.md) | `GET /v1beta/third-parties` | [docs](https://docs.atlar.com/v1/reference/get_v1beta-third-parties) |
| [V1BETA Read counterparty by its externalId](actions/v1beta-read-counterparty-by-its-externalid.md) | `GET /v1beta/counterparties:getByExternalId/{externalId}` | [docs](https://docs.atlar.com/v1/reference/get_v1beta-counterparties-getbyexternalid-externalid) |
| [V1BETA Read credit transfer by its externalId](actions/v1beta-read-credit-transfer-by-its-externalid.md) | `GET /v1beta/credit-transfers:getByExternalId/{externalId}` | [docs](https://docs.atlar.com/v1/reference/get_v1beta-credit-transfers-getbyexternalid-externalid) |
| [V1BETA Read Direct Debit by its externalId](actions/v1beta-read-direct-debit-by-its-externalid.md) | `GET /v1beta/direct-debits:getByExternalId/{externalId}` | [docs](https://docs.atlar.com/v1/reference/get_v1beta-direct-debits-getbyexternalid-externalid) |
| [V1BETA Read external account by its externalId](actions/v1beta-read-external-account-by-its-externalid.md) | `GET /v1beta/external-accounts:getByExternalId/{externalId}` | [docs](https://docs.atlar.com/v1/reference/get_v1beta-external-accounts-getbyexternalid-externalid) |
| [V1BETA Read Mandate by its externalId](actions/v1beta-read-mandate-by-its-externalid.md) | `GET /v1beta/mandates:getByExternalId/{externalId}` | [docs](https://docs.atlar.com/v1/reference/get_v1beta-mandates-getbyexternalid-externalid) |
| [V1BETA Read third party](actions/v1beta-read-third-party.md) | `GET /v1beta/third-parties/{id}` | [docs](https://docs.atlar.com/v1/reference/get_v1beta-third-parties-id) |
| [V1BETA Reconcile Expected Transaction](actions/v1beta-reconcile-expected-transaction.md) | `POST /v1beta/expected-transactions/{id}:reconcile` | [docs](https://docs.atlar.com/v1/reference/post_v1beta-expected-transactions-id-reconcile) |
| [V1BETA Unarchive Expected Transaction](actions/v1beta-unarchive-expected-transaction.md) | `POST /v1beta/expected-transactions/{id}:unarchive` | [docs](https://docs.atlar.com/v1/reference/post_v1beta-expected-transactions-id-unarchive) |
| [V1BETA Unreconcile Expected Transaction](actions/v1beta-unreconcile-expected-transaction.md) | `POST /v1beta/expected-transactions/{id}:unreconcile` | [docs](https://docs.atlar.com/v1/reference/post_v1beta-expected-transactions-id-unreconcile) |
