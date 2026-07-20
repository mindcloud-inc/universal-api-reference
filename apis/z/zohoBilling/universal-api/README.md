# <img src="https://images.mindcloud.co/apps/icons/205219029127785032_1775165810139.jpeg" alt="Zoho Billing logo" width="28" height="28"> Zoho Billing: Universal API

Manage subscriptions, customers, invoices, and billing catalogs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoBilling/latest
- **Category:** Commerce / Accounting
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/billing/
- **Vendor API docs:** https://www.zoho.com/billing/api/v1/introduction/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST |  |
| [List Customers](actions/list-customers.md) | GET |  |
| [Retrieve Customer](actions/retrieve-customer.md) | GET |  |
| [Update Customer](actions/update-customer.md) | PUT |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST |  |
| [List Invoices](actions/list-invoices.md) | GET |  |
| [Retrieve Invoice](actions/retrieve-invoice.md) | GET |  |
| [Update Invoice](actions/update-invoice.md) | PUT |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET |  |
| [List Organizations](actions/list-organizations.md) | GET |  |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [Create Plan](actions/create-plan.md) | POST |  |
| [List Plans](actions/list-plans.md) | GET |  |
| [Retrieve Plan](actions/retrieve-plan.md) | GET |  |
| [Update Plan](actions/update-plan.md) | PUT |  |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST |  |
| [List Products](actions/list-products.md) | GET |  |
| [Retrieve Product](actions/retrieve-product.md) | GET |  |
| [Update Product](actions/update-product.md) | PUT |  |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | PUT |  |
| [Create Subscription](actions/create-subscription.md) | POST |  |
| [List Subscriptions](actions/list-subscriptions.md) | GET |  |
| [Reactivate Subscription](actions/reactivate-subscription.md) | PUT |  |
| [Retrieve Subscription](actions/retrieve-subscription.md) | GET |  |
| [Update Subscription](actions/update-subscription.md) | PUT |  |

