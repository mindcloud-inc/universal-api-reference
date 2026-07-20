# <img src="https://images.mindcloud.co/apps/icons/unnamed-13_1774901445247.png" alt="Trolley logo" width="28" height="28"> Trolley: Universal API

Trolley payout and invoice management API integration.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/trolley/latest
- **Category:** Commerce / Accounting
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://trolley.com
- **Vendor API docs:** https://developers.trolley.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Recipients](actions/list-recipients.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trolley/latest/actions/list-recipients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Accounts

| Action | Method | Description |
| --- | --- | --- |
| [List Balances](actions/list-balances.md) | GET | Retrieves all account balances from Trolley. |
| [List PayPal Account Balances](actions/list-pay-pal-account-balances.md) | GET | Retrieves PayPal account balances from Trolley. |
| [List Trolley Account Balances](actions/list-trolley-account-balances.md) | GET | Retrieves Trolley account balances from Trolley. |

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [Get Country](actions/get-country.md) | GET | Retrieves a country from Trolley by country code. |

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [List Recipient Logs](actions/list-recipient-logs.md) | GET | Retrieves logs for a recipient from Trolley. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Recipient](actions/create-recipient.md) | POST | Creates a new recipient in Trolley. |
| [Delete Recipient](actions/delete-recipient.md) | DELETE | Deletes an existing recipient from Trolley. |
| [Get Recipient](actions/get-recipient.md) | GET | Retrieves a single recipient from Trolley. |
| [List Recipients](actions/list-recipients.md) | GET | Retrieves all recipient records from Trolley. |
| [Search Recipients](actions/search-recipients.md) | GET | Finds recipients in Trolley using search filters. |
| [Update Recipient](actions/update-recipient.md) | PUT | Updates an existing recipient in Trolley. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in Trolley. |
| [Create Invoice Lines](actions/create-invoice-lines.md) | POST | Creates new invoice lines in Trolley. |
| [Delete Invoice](actions/delete-invoice.md) | DELETE | Deletes an existing invoice from Trolley. |
| [Delete Invoice Lines](actions/delete-invoice-lines.md) | DELETE | Deletes existing invoice lines from Trolley. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves a single invoice from Trolley. |
| [Search Invoices](actions/search-invoices.md) | GET | Finds invoices in Trolley using search filters. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an existing invoice in Trolley. |
| [Update Invoice Lines](actions/update-invoice-lines.md) | PUT | Updates existing invoice lines in Trolley. |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [Create Recipient Account](actions/create-recipient-account.md) | POST | Creates a new recipient payment account in Trolley. |
| [Delete Recipient Account](actions/delete-recipient-account.md) | DELETE | Deletes a recipient payment account from Trolley. |
| [Get Recipient Account](actions/get-recipient-account.md) | GET | Retrieves a recipient payment account from Trolley. |
| [List Recipient Accounts](actions/list-recipient-accounts.md) | GET | Retrieves recipient payment accounts from Trolley. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Create Recipient Offline Payment](actions/create-recipient-offline-payment.md) | POST | Creates an offline payment for a recipient in Trolley. |
| [Delete Recipient Offline Payment](actions/delete-recipient-offline-payment.md) | DELETE | Deletes a recipient offline payment from Trolley. |
| [List Batches](actions/list-batches.md) | GET | Retrieves all payment batches from Trolley. |
| [List Offline Payments](actions/list-offline-payments.md) | GET | Retrieves all offline payments from Trolley. |
| [List Recipient Offline Payments](actions/list-recipient-offline-payments.md) | GET | Retrieves offline payments for a recipient from Trolley. |
| [List Recipient Payments](actions/list-recipient-payments.md) | GET | Retrieves payments for a recipient from Trolley. |
| [Search Invoice Payments](actions/search-invoice-payments.md) | GET | Finds invoice payments in Trolley using search filters. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Get Recipient Verifications](actions/get-recipient-verifications.md) | GET | Retrieves recipient verification results from Trolley. |
| [List Verifications](actions/list-verifications.md) | GET | Retrieves all verification records from Trolley. |

