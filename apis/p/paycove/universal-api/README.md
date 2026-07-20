# <img src="https://images.mindcloud.co/apps/icons/paycove_1774886481848.png" alt="Paycove logo" width="28" height="28"> Paycove: Universal API

Automate invoicing, payments, and financial reporting

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/paycove/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.paycove.io/
- **Vendor API docs:** https://docs.paycove.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Get Application Status](actions/get-application-status.md) | GET | Retrieves a gateway application status from Paycove. |
| [Start Or Continue Gateway Application](actions/start-or-continue-gateway-application.md) | POST | Starts or continues a gateway application in Paycove. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from Paycove. |
| [Get Contact Details](actions/get-contact-details.md) | GET | Retrieves a contact from Paycove. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Paycove. |
| [Update Contact](actions/update-contact.md) | PUT | Updates a contact in Paycove. |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST | Creates a deal in Paycove. |
| [Delete Deal](actions/delete-deal.md) | DELETE | Deletes a deal from Paycove. |
| [Get Deal Details](actions/get-deal-details.md) | GET | Retrieves a deal from Paycove. |
| [List Deals](actions/list-deals.md) | GET | Retrieves deals from Paycove. |
| [Reassign To New CRM Deal](actions/reassign-to-new-crm-deal.md) | PUT | Updates a Paycove deal with a new CRM deal ID. |

### Deals

| Action | Method | Description |
| --- | --- | --- |
| [List Deal Scheduled Payments](actions/list-deal-scheduled-payments.md) | GET | Retrieves scheduled payments for a Paycove deal. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Delete Organization](actions/delete-organization.md) | DELETE | Deletes an organization from Paycove. |
| [Get Organization Details](actions/get-organization-details.md) | GET | Retrieves an organization from Paycove. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from Paycove. |
| [Update Organization](actions/update-organization.md) | PUT | Updates an organization in Paycove. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST | Creates an account in Paycove. |
| [Create Checkout Session](actions/create-checkout-session.md) | POST | Creates a checkout session in Paycove. |
| [Create Deal Scheduled Payments](actions/create-deal-scheduled-payments.md) | POST | Creates scheduled payments for a Paycove deal. |
| [Create Fee](actions/create-fee.md) | POST | Creates a fee for a Paycove deal. |
| [Invite Users](actions/invite-users.md) | POST | Invites users to a Paycove account. |
| [Legal Accept](actions/legal-accept.md) | POST | Creates a legal acceptance token in Paycove. |
| [Update Deal Scheduled Payments](actions/update-deal-scheduled-payments.md) | PUT | Updates scheduled payments for a Paycove deal. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [List Scheduled Payments](actions/list-scheduled-payments.md) | GET | Retrieves scheduled payments from Paycove. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a product in Paycove. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes a product from Paycove. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Paycove. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Paycove. |
| [Update Product](actions/update-product.md) | PUT | Updates a product in Paycove. |

### Refund

| Action | Method | Description |
| --- | --- | --- |
| [Issue Refund](actions/issue-refund.md) | POST | Issues a refund in Paycove. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Paycove. |

### Webhook Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST | Creates a webhook subscription in Paycove. |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | DELETE | Deletes a webhook subscription from Paycove. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhook subscriptions from Paycove. |

