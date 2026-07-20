# OPN: Native API Reference

A consolidated summary of OPN's API configuration and 113 documented operations, with links to official documentation.

- **Official docs:** https://docs.omise.co
- **OpenAPI specification:** https://api.omise.co/schema
- **API base URL:** `https://api.omise.co`

## Authentication

### Secret Key

Use your OPN secret key as the Basic Auth username. Leave password blank unless your tenant requires otherwise.

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

[Official authentication documentation](https://docs.omise.co/en/how-to-access-omise-api-keys)

## Pagination

Use `limit` in the query string to set the page size (default 20; minimum 1). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (113 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept Dispute](actions/accept-dispute.md) | `PATCH /disputes/:id/accept` | [docs](https://docs.omise.co/disputes-api) |
| [Authorize Chain](actions/authorize-chain.md) | `POST /chains/:id/authorize` | [docs](https://docs.omise.co) |
| [Capture Charge](actions/capture-charge.md) | `POST /charges/:id/capture` | [docs](https://docs.omise.co/charge-api) |
| [Close Dispute](actions/close-dispute.md) | `PATCH /disputes/:id/close` | [docs](https://docs.omise.co/disputes-api) |
| [Create Charge](actions/create-charge.md) | `POST /charges` | [docs](https://docs.omise.co/charge-api) |
| [Create Charge Refund](actions/create-charge-refund.md) | `POST /charges/:id/refunds` | [docs](https://docs.omise.co/refunds-api) |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://docs.omise.co/customer-api) |
| [Create Dispute](actions/create-dispute.md) | `POST /charges/:id/disputes` | [docs](https://docs.omise.co/disputes-api) |
| [Create Dispute Document](actions/create-dispute-document.md) | `POST /disputes/:id/documents` | [docs](https://docs.omise.co/disputes-api) |
| [Create Link](actions/create-link.md) | `POST /links` | [docs](https://docs.omise.co/links-api) |
| [Create Linked Account](actions/create-linked-account.md) | `POST /linked_accounts` | [docs](https://docs.omise.co) |
| [Create MFA Confirmation](actions/create-mfa-confirmation.md) | `POST /mfa_confirmations` | [docs](https://docs.omise.co) |
| [Create Recipient](actions/create-recipient.md) | `POST /recipients` | [docs](https://docs.omise.co/recipient-api) |
| [Create Schedule](actions/create-schedule.md) | `POST /schedules` | [docs](https://docs.omise.co/schedules-api) |
| [Create Source](actions/create-source.md) | `POST /sources` | [docs](https://docs.omise.co/source-api) |
| [Create Sub Merchant](actions/create-sub-merchant.md) | `POST /sub_merchants` | [docs](https://docs.omise.co) |
| [Create Transfer](actions/create-transfer.md) | `POST /transfers` | [docs](https://docs.omise.co/transfer-api) |
| [Create Webhook Secret](actions/create-webhook-secret.md) | `POST /webhooks/secrets` | [docs](https://docs.omise.co) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /customers/:id` | [docs](https://docs.omise.co/customer-api) |
| [Delete Customer Card](actions/delete-customer-card.md) | `DELETE /customers/:id/cards/:cardId` | [docs](https://docs.omise.co/card-api) |
| [Delete Dispute Document](actions/delete-dispute-document.md) | `DELETE /disputes/:id/documents/:documentId` | [docs](https://docs.omise.co/disputes-api) |
| [Delete Link](actions/delete-link.md) | `DELETE /links/:id` | [docs](https://docs.omise.co/links-api) |
| [Delete Linked Account](actions/delete-linked-account.md) | `DELETE /linked_accounts/:id` | [docs](https://docs.omise.co) |
| [Delete Recipient](actions/delete-recipient.md) | `DELETE /recipients/:id` | [docs](https://docs.omise.co/recipient-api) |
| [Delete Schedule](actions/delete-schedule.md) | `DELETE /schedules/:id` | [docs](https://docs.omise.co/schedules-api) |
| [Delete Transfer](actions/delete-transfer.md) | `DELETE /transfers/:id` | [docs](https://docs.omise.co/transfer-api) |
| [Delete Webhook Secret](actions/delete-webhook-secret.md) | `DELETE /webhooks/secrets/:id` | [docs](https://docs.omise.co) |
| [Expire Charge](actions/expire-charge.md) | `POST /charges/:id/expire` | [docs](https://docs.omise.co/charge-api) |
| [Get API Schema](actions/get-api-schema.md) | `GET /schema` | [docs](https://docs.omise.co/using-the-api-schema) |
| [Get Balance](actions/get-balance.md) | `GET /balance` | [docs](https://docs.omise.co/balance-api) |
| [Get Capability](actions/get-capability.md) | `GET /capability` | [docs](https://docs.omise.co/capability-api) |
| [Get Chain](actions/get-chain.md) | `GET /chains/:id` | [docs](https://docs.omise.co) |
| [Get Chain Account](actions/get-chain-account.md) | `GET /chains/:id/account` | [docs](https://docs.omise.co) |
| [Get Charge](actions/get-charge.md) | `GET /charges/:id` | [docs](https://docs.omise.co/charge-api) |
| [Get Charge Refund](actions/get-charge-refund.md) | `GET /charges/:id/refunds/:refundId` | [docs](https://docs.omise.co/refunds-api) |
| [Get Customer](actions/get-customer.md) | `GET /customers/:id` | [docs](https://docs.omise.co/customer-api) |
| [Get Customer Card](actions/get-customer-card.md) | `GET /customers/:id/cards/:cardId` | [docs](https://docs.omise.co/card-api) |
| [Get Dispute](actions/get-dispute.md) | `GET /disputes/:id` | [docs](https://docs.omise.co/disputes-api) |
| [Get Dispute Document](actions/get-dispute-document.md) | `GET /disputes/:id/documents/:documentId` | [docs](https://docs.omise.co/disputes-api) |
| [Get Event](actions/get-event.md) | `GET /events/:id` | [docs](https://docs.omise.co/events-api) |
| [Get Forex Rate](actions/get-forex-rate.md) | `GET /forex/:currency` | [docs](https://docs.omise.co) |
| [Get Link](actions/get-link.md) | `GET /links/:id` | [docs](https://docs.omise.co/links-api) |
| [Get Linked Account](actions/get-linked-account.md) | `GET /linked_accounts/:id` | [docs](https://docs.omise.co) |
| [Get Occurrence](actions/get-occurrence.md) | `GET /occurrences/:id` | [docs](https://docs.omise.co/schedules-api) |
| [Get Receipt](actions/get-receipt.md) | `GET /receipts/:id` | [docs](https://docs.omise.co) |
| [Get Recipient](actions/get-recipient.md) | `GET /recipients/:id` | [docs](https://docs.omise.co/recipient-api) |
| [Get Schedule](actions/get-schedule.md) | `GET /schedules/:id` | [docs](https://docs.omise.co/schedules-api) |
| [Get Source](actions/get-source.md) | `GET /sources/:id` | [docs](https://docs.omise.co/source-api) |
| [Get System Info](actions/get-system-info.md) | `GET /` | [docs](https://docs.omise.co) |
| [Get Transaction](actions/get-transaction.md) | `GET /transactions/:id` | [docs](https://docs.omise.co) |
| [Get Transfer](actions/get-transfer.md) | `GET /transfers/:id` | [docs](https://docs.omise.co/transfer-api) |
| [Get Webhook Secret](actions/get-webhook-secret.md) | `GET /webhooks/secrets/:id` | [docs](https://docs.omise.co) |
| [Global Search](actions/global-search.md) | `GET /search` | [docs](https://docs.omise.co/search-query-and-filters) |
| [List Account API Versions](actions/list-account-api-versions.md) | `GET /account/api_versions` | [docs](https://docs.omise.co/api-versioning) |
| [List Chain Keys](actions/list-chain-keys.md) | `GET /chains/:id/keys` | [docs](https://docs.omise.co) |
| [List Chains](actions/list-chains.md) | `GET /chains` | [docs](https://docs.omise.co) |
| [List Charge Events](actions/list-charge-events.md) | `GET /charges/:id/events` | [docs](https://docs.omise.co/events-api) |
| [List Charge Refunds](actions/list-charge-refunds.md) | `GET /charges/:id/refunds` | [docs](https://docs.omise.co/refunds-api) |
| [List Charge Schedules](actions/list-charge-schedules.md) | `GET /charges/schedules` | [docs](https://docs.omise.co/schedules-api) |
| [List Charges](actions/list-charges.md) | `GET /charges` | [docs](https://docs.omise.co/charge-api) |
| [List Closed Disputes](actions/list-closed-disputes.md) | `GET /disputes/closed` | [docs](https://docs.omise.co/disputes-api) |
| [List Customer Cards](actions/list-customer-cards.md) | `GET /customers/:id/cards` | [docs](https://docs.omise.co/card-api) |
| [List Customer Schedules](actions/list-customer-schedules.md) | `GET /customers/:id/schedules` | [docs](https://docs.omise.co/schedules-api) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://docs.omise.co/customer-api) |
| [List Dispute Documents](actions/list-dispute-documents.md) | `GET /disputes/:id/documents` | [docs](https://docs.omise.co/disputes-api) |
| [List Disputes](actions/list-disputes.md) | `GET /disputes` | [docs](https://docs.omise.co/disputes-api) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://docs.omise.co/events-api) |
| [List Link Charges](actions/list-link-charges.md) | `GET /links/:id/charges` | [docs](https://docs.omise.co/links-api) |
| [List Linked Accounts](actions/list-linked-accounts.md) | `GET /linked_accounts` | [docs](https://docs.omise.co) |
| [List Links](actions/list-links.md) | `GET /links` | [docs](https://docs.omise.co/links-api) |
| [List Open Disputes](actions/list-open-disputes.md) | `GET /disputes/open` | [docs](https://docs.omise.co/disputes-api) |
| [List Pending Disputes](actions/list-pending-disputes.md) | `GET /disputes/pending` | [docs](https://docs.omise.co/disputes-api) |
| [List Receipts](actions/list-receipts.md) | `GET /receipts` | [docs](https://docs.omise.co) |
| [List Recipient Schedules](actions/list-recipient-schedules.md) | `GET /recipients/:id/schedules` | [docs](https://docs.omise.co/schedules-api) |
| [List Recipients](actions/list-recipients.md) | `GET /recipients` | [docs](https://docs.omise.co/recipient-api) |
| [List Refunds](actions/list-refunds.md) | `GET /refunds` | [docs](https://docs.omise.co/refunds-api) |
| [List Routing Group Rules](actions/list-routing-group-rules.md) | `GET /routing_group_rules` | [docs](https://docs.omise.co) |
| [List Schedule Occurrences](actions/list-schedule-occurrences.md) | `GET /schedules/:id/occurrences` | [docs](https://docs.omise.co/schedules-api) |
| [List Schedules](actions/list-schedules.md) | `GET /schedules` | [docs](https://docs.omise.co/schedules-api) |
| [List Sub Merchants](actions/list-sub-merchants.md) | `GET /sub_merchants` | [docs](https://docs.omise.co) |
| [List Transactions](actions/list-transactions.md) | `GET /transactions` | [docs](https://docs.omise.co) |
| [List Transfer Schedules](actions/list-transfer-schedules.md) | `GET /transfers/schedules` | [docs](https://docs.omise.co/schedules-api) |
| [List Transfers](actions/list-transfers.md) | `GET /transfers` | [docs](https://docs.omise.co/transfer-api) |
| [List Webhook Secrets](actions/list-webhook-secrets.md) | `GET /webhooks/secrets` | [docs](https://docs.omise.co) |
| [Mark Charge As Failed](actions/mark-charge-as-failed.md) | `POST /charges/:id/mark_as_failed` | [docs](https://docs.omise.co/charge-api) |
| [Mark Charge As Paid](actions/mark-charge-as-paid.md) | `POST /charges/:id/mark_as_paid` | [docs](https://docs.omise.co/charge-api) |
| [Mark Transfer As Paid](actions/mark-transfer-as-paid.md) | `POST /transfers/:id/mark_as_paid` | [docs](https://docs.omise.co/transfer-api) |
| [Mark Transfer As Sent](actions/mark-transfer-as-sent.md) | `POST /transfers/:id/mark_as_sent` | [docs](https://docs.omise.co/transfer-api) |
| [Reverse Charge](actions/reverse-charge.md) | `POST /charges/:id/reverse` | [docs](https://docs.omise.co/charge-api) |
| [Revoke Chain](actions/revoke-chain.md) | `POST /chains/:id/revoke` | [docs](https://docs.omise.co) |
| [Search Audits](actions/search-audits.md) | `GET /audits/search` | [docs](https://docs.omise.co) |
| [Search Charge Schedules](actions/search-charge-schedules.md) | `GET /charges/schedules/search` | [docs](https://docs.omise.co/search-query-and-filters) |
| [Search Charges](actions/search-charges.md) | `GET /charges/search` | [docs](https://docs.omise.co/search-query-and-filters) |
| [Search Customers](actions/search-customers.md) | `GET /customers/search` | [docs](https://docs.omise.co/search-query-and-filters) |
| [Search Disputes](actions/search-disputes.md) | `GET /disputes/search` | [docs](https://docs.omise.co/search-query-and-filters) |
| [Search Linked Accounts](actions/search-linked-accounts.md) | `GET /linked_accounts/search` | [docs](https://docs.omise.co/search-query-and-filters) |
| [Search Links](actions/search-links.md) | `GET /links/search` | [docs](https://docs.omise.co/search-query-and-filters) |
| [Search Receipts](actions/search-receipts.md) | `GET /receipts/receipts/search` | [docs](https://docs.omise.co/search-query-and-filters) |
| [Search Recipients](actions/search-recipients.md) | `GET /recipients/search` | [docs](https://docs.omise.co/search-query-and-filters) |
| [Search Refunds](actions/search-refunds.md) | `GET /refunds/search` | [docs](https://docs.omise.co/search-query-and-filters) |
| [Search Sub Merchants](actions/search-sub-merchants.md) | `GET /sub_merchants/search` | [docs](https://docs.omise.co/search-query-and-filters) |
| [Search Transfer Schedules](actions/search-transfer-schedules.md) | `GET /transfers/schedules/search` | [docs](https://docs.omise.co/search-query-and-filters) |
| [Search Transfers](actions/search-transfers.md) | `GET /transfers/search` | [docs](https://docs.omise.co/search-query-and-filters) |
| [Update Account](actions/update-account.md) | `PATCH /account` | [docs](https://docs.omise.co) |
| [Update Account API Version](actions/update-account-api-version.md) | `PATCH /account/api_version` | [docs](https://docs.omise.co/api-versioning) |
| [Update Charge](actions/update-charge.md) | `PATCH /charges/:id` | [docs](https://docs.omise.co/charge-api) |
| [Update Consent](actions/update-consent.md) | `PATCH /consent` | [docs](https://docs.omise.co) |
| [Update Customer](actions/update-customer.md) | `PATCH /customers/:id` | [docs](https://docs.omise.co/customer-api) |
| [Update Customer Card](actions/update-customer-card.md) | `PATCH /customers/:id/cards/:cardId` | [docs](https://docs.omise.co/card-api) |
| [Update Dispute](actions/update-dispute.md) | `PATCH /disputes/:id` | [docs](https://docs.omise.co/disputes-api) |
| [Update Recipient](actions/update-recipient.md) | `PATCH /recipients/:id` | [docs](https://docs.omise.co/recipient-api) |
| [Update Transfer](actions/update-transfer.md) | `PATCH /transfers/:id` | [docs](https://docs.omise.co/transfer-api) |
| [Verify Recipient](actions/verify-recipient.md) | `PATCH /recipients/:id/verify` | [docs](https://docs.omise.co/recipient-api) |
