# <img src="https://images.mindcloud.co/apps/icons/android-icon-144x144_1776882724813.png" alt="Merit logo" width="28" height="28"> Merit: Universal API

Manage accounting, invoices, customers, vendors, and reports in Merit

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/merit/latest
- **Category:** Commerce / Accounting
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.merit.ee/en/merit-aktiva/
- **Vendor API docs:** https://api.merit.ee/merit-aktiva-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Taxes](actions/list-taxes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-taxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Bill

| Action | Method | Description |
| --- | --- | --- |
| [Create Purchase Invoice](actions/create-purchase-invoice.md) | POST |  |
| [Get Purchase Invoice Details](actions/get-purchase-invoice-details.md) | GET |  |
| [List Purchase Invoices](actions/list-purchase-invoices.md) | GET |  |

### Bills

| Action | Method | Description |
| --- | --- | --- |
| [Delete Purchase Invoice](actions/delete-purchase-invoice.md) | DELETE |  |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST |  |
| [List Customers](actions/list-customers.md) | GET |  |
| [Update Customer](actions/update-customer.md) | PUT |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Sales Invoice PDF](actions/get-sales-invoice-pdf.md) | GET |  |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Group](actions/create-customer-group.md) | POST |  |
| [Create Item Group](actions/create-item-group.md) | POST |  |
| [List Item Groups](actions/list-item-groups.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Credit Invoice](actions/create-credit-invoice.md) | POST |  |
| [Create Invoice From Sales Offer](actions/create-invoice-from-sales-offer.md) | POST |  |
| [Create Sales Invoice](actions/create-sales-invoice.md) | POST |  |
| [Delete Sales Invoice](actions/delete-sales-invoice.md) | DELETE |  |
| [Get Sales Invoice Details](actions/get-sales-invoice-details.md) | GET |  |
| [List Sales Invoices](actions/list-sales-invoices.md) | GET |  |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | POST |  |
| [List Items](actions/list-items.md) | GET |  |
| [Update Item](actions/update-item.md) | PUT |  |

### Offers

| Action | Method | Description |
| --- | --- | --- |
| [Create Sales Offer](actions/create-sales-offer.md) | POST |  |
| [Get Sales Offer Details](actions/get-sales-offer-details.md) | GET |  |
| [List Sales Offers](actions/list-sales-offers.md) | GET |  |
| [Update Sales Offer](actions/update-sales-offer.md) | PUT |  |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Types](actions/list-payment-types.md) | GET |  |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Of Purchase Invoice](actions/create-payment-of-purchase-invoice.md) | POST |  |
| [Create Payment Of Sales Invoice](actions/create-payment-of-sales-invoice.md) | POST |  |
| [Create Payment Of Sales Offer](actions/create-payment-of-sales-offer.md) | POST |  |
| [Delete Payment](actions/delete-payment.md) | DELETE |  |
| [List Payments](actions/list-payments.md) | GET |  |

### Purchase Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Purchase Invoice Waiting Approval](actions/create-purchase-invoice-waiting-approval.md) | POST |  |

### Recurring Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Recurring Invoice](actions/create-recurring-invoice.md) | POST |  |
| [Get Recurring Invoice Details](actions/get-recurring-invoice-details.md) | GET |  |
| [List Recurring Invoices](actions/list-recurring-invoices.md) | GET |  |

### Tax Rate

| Action | Method | Description |
| --- | --- | --- |
| [List Taxes](actions/list-taxes.md) | GET |  |

### Vendor

| Action | Method | Description |
| --- | --- | --- |
| [Create Vendor](actions/create-vendor.md) | POST |  |
| [List Vendors](actions/list-vendors.md) | GET |  |

