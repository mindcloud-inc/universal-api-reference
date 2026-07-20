# <img src="https://images.mindcloud.co/apps/icons/opn-omise-icon-32_1775745185032.png" alt="OPN logo" width="28" height="28"> OPN: Universal API

Create and manage charges, customers, disputes, links, recipients, schedules, refunds, and transfers in OPN's server-side payments API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oPN/latest
- **Category:** Commerce
- **Actions:** 113
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.omise.co
- **Vendor API docs:** https://docs.omise.co

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Balance](actions/get-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (113)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [List Account API Versions](actions/list-account-api-versions.md) | GET | Retrieves a list of account API versions from OPN. |
| [Update Account](actions/update-account.md) | PUT | Updates existing account details in OPN. |
| [Update Account API Version](actions/update-account-api-version.md) | PUT | Updates the account API version in OPN. |

### Audit

| Action | Method | Description |
| --- | --- | --- |
| [Search Audits](actions/search-audits.md) | GET | Finds audit records in OPN by search criteria. |

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | GET | Retrieves account balance details from OPN. |

### Capability

| Action | Method | Description |
| --- | --- | --- |
| [Get Capability](actions/get-capability.md) | GET | Retrieves account capability details from OPN. |

### Card

| Action | Method | Description |
| --- | --- | --- |
| [Delete Customer Card](actions/delete-customer-card.md) | DELETE | Deletes an existing customer card from OPN. |
| [Get Customer Card](actions/get-customer-card.md) | GET | Retrieves details for a customer card from OPN. |
| [List Customer Cards](actions/list-customer-cards.md) | GET | Retrieves a list of cards for a customer from OPN. |
| [Update Customer Card](actions/update-customer-card.md) | PUT | Updates an existing customer card in OPN. |

### Chain

| Action | Method | Description |
| --- | --- | --- |
| [Authorize Chain](actions/authorize-chain.md) | PUT | Authorizes an existing chain in OPN. |
| [Get Chain](actions/get-chain.md) | GET | Retrieves details for a chain from OPN. |
| [Get Chain Account](actions/get-chain-account.md) | GET | Retrieves account details for a chain from OPN. |
| [List Chain Keys](actions/list-chain-keys.md) | GET | Retrieves a list of keys for a chain from OPN. |
| [List Chains](actions/list-chains.md) | GET | Retrieves a list of chains from OPN. |
| [Revoke Chain](actions/revoke-chain.md) | PUT | Revokes an existing chain in OPN. |

### Charge Schedule

| Action | Method | Description |
| --- | --- | --- |
| [List Charge Schedules](actions/list-charge-schedules.md) | GET | Retrieves a list of charge Schedules from OPN. |
| [Search Charge Schedules](actions/search-charge-schedules.md) | GET | Finds charge Schedules in OPN by search criteria. |

### Charges

| Action | Method | Description |
| --- | --- | --- |
| [Capture Charge](actions/capture-charge.md) | PUT | Captures an existing charge in OPN. |
| [Create Charge](actions/create-charge.md) | POST | Creates a new charge in OPN. |
| [Expire Charge](actions/expire-charge.md) | PUT | Expires an existing charge in OPN. |
| [Get Charge](actions/get-charge.md) | GET | Retrieves details for a charge from OPN. |
| [List Charges](actions/list-charges.md) | GET | Retrieves a list of charges from OPN. |
| [List Link Charges](actions/list-link-charges.md) | GET | Retrieves a list of charges for a link from OPN. |
| [Mark Charge As Failed](actions/mark-charge-as-failed.md) | PUT | Marks an existing charge as failed in OPN. |
| [Mark Charge As Paid](actions/mark-charge-as-paid.md) | PUT | Marks an existing charge as paid in OPN. |
| [Reverse Charge](actions/reverse-charge.md) | PUT | Reverses an existing charge in OPN. |
| [Search Charges](actions/search-charges.md) | GET | Finds charges in OPN by search criteria. |
| [Update Charge](actions/update-charge.md) | PUT | Updates an existing charge in OPN. |

### Consent

| Action | Method | Description |
| --- | --- | --- |
| [Update Consent](actions/update-consent.md) | PUT | Updates existing consent details in OPN. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in OPN. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from OPN. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves details for a customer from OPN. |
| [List Customers](actions/list-customers.md) | GET | Retrieves a list of customers from OPN. |
| [Search Customers](actions/search-customers.md) | GET | Finds customers in OPN by search criteria. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in OPN. |

### Disputes

| Action | Method | Description |
| --- | --- | --- |
| [Accept Dispute](actions/accept-dispute.md) | PUT | Accepts an existing dispute in OPN. |
| [Close Dispute](actions/close-dispute.md) | PUT | Closes an existing dispute in OPN. |
| [Create Dispute](actions/create-dispute.md) | POST | Creates a new dispute in OPN. |
| [Get Dispute](actions/get-dispute.md) | GET | Retrieves details for a dispute from OPN. |
| [List Closed Disputes](actions/list-closed-disputes.md) | GET | Retrieves a list of closed Disputes from OPN. |
| [List Disputes](actions/list-disputes.md) | GET | Retrieves a list of disputes from OPN. |
| [List Open Disputes](actions/list-open-disputes.md) | GET | Retrieves a list of open Disputes from OPN. |
| [List Pending Disputes](actions/list-pending-disputes.md) | GET | Retrieves a list of pending Disputes from OPN. |
| [Search Disputes](actions/search-disputes.md) | GET | Finds disputes in OPN by search criteria. |
| [Update Dispute](actions/update-dispute.md) | PUT | Updates an existing dispute in OPN. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Dispute Document](actions/create-dispute-document.md) | POST | Creates a new document for a dispute in OPN. |
| [Delete Dispute Document](actions/delete-dispute-document.md) | DELETE | Deletes an existing dispute document from OPN. |
| [Get Dispute Document](actions/get-dispute-document.md) | GET | Retrieves details for a dispute document from OPN. |
| [List Dispute Documents](actions/list-dispute-documents.md) | GET | Retrieves a list of documents for a dispute from OPN. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves details for an event from OPN. |
| [List Events](actions/list-events.md) | GET | Retrieves a list of events from OPN. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List Charge Events](actions/list-charge-events.md) | GET | Retrieves a list of events for a charge from OPN. |

### Forex

| Action | Method | Description |
| --- | --- | --- |
| [Get Forex Rate](actions/get-forex-rate.md) | GET | Retrieves a forex rate from OPN. |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Link](actions/create-link.md) | POST | Creates a new link in OPN. |
| [Delete Link](actions/delete-link.md) | DELETE | Deletes an existing link from OPN. |
| [Get Link](actions/get-link.md) | GET | Retrieves details for a link from OPN. |
| [List Links](actions/list-links.md) | GET | Retrieves a list of links from OPN. |
| [Search Links](actions/search-links.md) | GET | Finds links in OPN by search criteria. |

### Linked Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Linked Account](actions/create-linked-account.md) | POST | Creates a new linked Account in OPN. |
| [Delete Linked Account](actions/delete-linked-account.md) | DELETE | Deletes an existing linked Account from OPN. |
| [Get Linked Account](actions/get-linked-account.md) | GET | Retrieves details for a linked Account from OPN. |
| [List Linked Accounts](actions/list-linked-accounts.md) | GET | Retrieves a list of linked Accounts from OPN. |
| [Search Linked Accounts](actions/search-linked-accounts.md) | GET | Finds linked Accounts in OPN by search criteria. |

### Mfa Confirmation

| Action | Method | Description |
| --- | --- | --- |
| [Create MFA Confirmation](actions/create-mfa-confirmation.md) | POST | Creates a new MFA confirmation in OPN. |

### Occurrence

| Action | Method | Description |
| --- | --- | --- |
| [Get Occurrence](actions/get-occurrence.md) | GET | Retrieves details for a schedule occurrence from OPN. |
| [List Schedule Occurrences](actions/list-schedule-occurrences.md) | GET | Retrieves a list of occurrences for a schedule from OPN. |

### Receipt

| Action | Method | Description |
| --- | --- | --- |
| [Get Receipt](actions/get-receipt.md) | GET | Retrieves details for a receipt from OPN. |
| [List Receipts](actions/list-receipts.md) | GET | Retrieves a list of receipts from OPN. |
| [Search Receipts](actions/search-receipts.md) | GET | Finds receipts in OPN by search criteria. |

### Recipient

| Action | Method | Description |
| --- | --- | --- |
| [Create Recipient](actions/create-recipient.md) | POST | Creates a new recipient in OPN. |
| [Delete Recipient](actions/delete-recipient.md) | DELETE | Deletes an existing recipient from OPN. |
| [Get Recipient](actions/get-recipient.md) | GET | Retrieves details for a recipient from OPN. |
| [List Recipients](actions/list-recipients.md) | GET | Retrieves a list of recipients from OPN. |
| [Search Recipients](actions/search-recipients.md) | GET | Finds recipients in OPN by search criteria. |
| [Update Recipient](actions/update-recipient.md) | PUT | Updates an existing recipient in OPN. |
| [Verify Recipient](actions/verify-recipient.md) | PUT | Verifies an existing recipient in OPN. |

### Refunds

| Action | Method | Description |
| --- | --- | --- |
| [Create Charge Refund](actions/create-charge-refund.md) | POST | Creates a new refund for a charge in OPN. |
| [Get Charge Refund](actions/get-charge-refund.md) | GET | Retrieves details for a charge refund from OPN. |
| [List Charge Refunds](actions/list-charge-refunds.md) | GET | Retrieves a list of refunds for a charge from OPN. |
| [List Refunds](actions/list-refunds.md) | GET | Retrieves a list of refunds from OPN. |
| [Search Refunds](actions/search-refunds.md) | GET | Finds refunds in OPN by search criteria. |

### Routing Group Rule

| Action | Method | Description |
| --- | --- | --- |
| [List Routing Group Rules](actions/list-routing-group-rules.md) | GET | Retrieves a list of routing Group Rules from OPN. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Create Schedule](actions/create-schedule.md) | POST | Creates a new schedule in OPN. |
| [Delete Schedule](actions/delete-schedule.md) | DELETE | Deletes an existing schedule from OPN. |
| [Get Schedule](actions/get-schedule.md) | GET | Retrieves details for a schedule from OPN. |
| [List Customer Schedules](actions/list-customer-schedules.md) | GET | Retrieves a list of schedules for a customer from OPN. |
| [List Recipient Schedules](actions/list-recipient-schedules.md) | GET | Retrieves a list of schedules for a recipient from OPN. |
| [List Schedules](actions/list-schedules.md) | GET | Retrieves a list of schedules from OPN. |

### Schema

| Action | Method | Description |
| --- | --- | --- |
| [Get API Schema](actions/get-api-schema.md) | GET | Retrieves the API schema from OPN. |

### Search

| Action | Method | Description |
| --- | --- | --- |
| [Global Search](actions/global-search.md) | GET | Finds records across OPN resources by search query. |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [Create Source](actions/create-source.md) | POST | Creates a new source in OPN. |
| [Get Source](actions/get-source.md) | GET | Retrieves details for a source from OPN. |

### Sub Merchant

| Action | Method | Description |
| --- | --- | --- |
| [Create Sub Merchant](actions/create-sub-merchant.md) | POST | Creates a new sub Merchant in OPN. |
| [List Sub Merchants](actions/list-sub-merchants.md) | GET | Retrieves a list of sub Merchants from OPN. |
| [Search Sub Merchants](actions/search-sub-merchants.md) | GET | Finds sub Merchants in OPN by search criteria. |

### System Info

| Action | Method | Description |
| --- | --- | --- |
| [Get System Info](actions/get-system-info.md) | GET | Retrieves system information details from OPN. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves details for a transaction from OPN. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves a list of transactions from OPN. |

### Transfer

| Action | Method | Description |
| --- | --- | --- |
| [Create Transfer](actions/create-transfer.md) | POST | Creates a new transfer in OPN. |
| [Delete Transfer](actions/delete-transfer.md) | DELETE | Deletes an existing transfer from OPN. |
| [Get Transfer](actions/get-transfer.md) | GET | Retrieves details for a transfer from OPN. |
| [List Transfers](actions/list-transfers.md) | GET | Retrieves a list of transfers from OPN. |
| [Mark Transfer As Paid](actions/mark-transfer-as-paid.md) | PUT | Marks an existing transfer as paid in OPN. |
| [Mark Transfer As Sent](actions/mark-transfer-as-sent.md) | PUT | Marks an existing transfer as sent in OPN. |
| [Search Transfers](actions/search-transfers.md) | GET | Finds transfers in OPN by search criteria. |
| [Update Transfer](actions/update-transfer.md) | PUT | Updates an existing transfer in OPN. |

### Transfer Schedule

| Action | Method | Description |
| --- | --- | --- |
| [List Transfer Schedules](actions/list-transfer-schedules.md) | GET | Retrieves a list of transfer Schedules from OPN. |
| [Search Transfer Schedules](actions/search-transfer-schedules.md) | GET | Finds transfer Schedules in OPN by search criteria. |

### Webhook Secret

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Secret](actions/create-webhook-secret.md) | POST | Creates a new webhook Secret in OPN. |
| [Delete Webhook Secret](actions/delete-webhook-secret.md) | DELETE | Deletes an existing webhook Secret from OPN. |
| [Get Webhook Secret](actions/get-webhook-secret.md) | GET | Retrieves details for a webhook Secret from OPN. |
| [List Webhook Secrets](actions/list-webhook-secrets.md) | GET | Retrieves a list of webhook Secrets from OPN. |

