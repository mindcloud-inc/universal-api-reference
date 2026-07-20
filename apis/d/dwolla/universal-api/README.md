# <img src="https://images.mindcloud.co/apps/icons/images-7_1775852754638.jpeg" alt="Dwolla logo" width="28" height="28"> Dwolla: Universal API

Dwolla provides ACH and account-to-account payment APIs for customers, funding sources, transfers, labels, events, and webhook subscriptions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dwolla/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.dwolla.com
- **Vendor API docs:** https://developers.dwolla.com/docs/api-reference/root

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Root](actions/get-root.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-root?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Bank Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Create Account Funding Source](actions/create-account-funding-source.md) | POST | Creates a funding source for a Dwolla account. |
| [Create Customer Funding Source](actions/create-customer-funding-source.md) | POST | Creates a funding source for a Dwolla customer. |
| [Get Funding Source](actions/get-funding-source.md) | GET | Retrieves details for a funding source from Dwolla. |
| [Get Funding Source Balance](actions/get-funding-source-balance.md) | GET | Retrieves balance details for a funding source in Dwolla. |
| [List Account Funding Sources](actions/list-account-funding-sources.md) | GET | Retrieves funding sources for a Dwolla account. |
| [List Customer Funding Sources](actions/list-customer-funding-sources.md) | GET | Retrieves funding sources for a Dwolla customer. |
| [Remove Funding Source](actions/remove-funding-source.md) | DELETE | Soft deletes a funding source from Dwolla. |
| [Update Funding Source](actions/update-funding-source.md) | PUT | Updates a bank funding source in Dwolla. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get Business Classification](actions/get-business-classification.md) | GET | Retrieves a business classification from Dwolla. |
| [List Business Classifications](actions/list-business-classifications.md) | GET | Retrieves a list of business classifications from Dwolla. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Dwolla. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves details for a customer from Dwolla. |
| [List Customers](actions/list-customers.md) | GET | Finds customers in Dwolla by search or filters. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Dwolla. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Transfer](actions/cancel-transfer.md) | PUT | Cancels a pending transfer in Dwolla. |
| [Create Transfer](actions/create-transfer.md) | POST | Creates a new transfer in Dwolla. |
| [Get Transfer](actions/get-transfer.md) | GET | Retrieves details for a transfer from Dwolla. |
| [List Account Transfers](actions/list-account-transfers.md) | GET | Finds transfers for a Dwolla account by filters. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves details for a Dwolla account. |
| [Get Root](actions/get-root.md) | GET | Retrieves the API root for accessible Dwolla resources. |
| [List Events](actions/list-events.md) | GET | Retrieves a list of events from Dwolla. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST | Creates a webhook subscription in Dwolla. |
| [Get Webhook Subscription](actions/get-webhook-subscription.md) | GET | Retrieves a webhook subscription from Dwolla. |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | GET | Retrieves a list of webhook subscriptions from Dwolla. |

