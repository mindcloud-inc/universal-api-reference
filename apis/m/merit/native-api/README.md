# Merit: Native API Reference

A consolidated summary of Merit's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://api.merit.ee/merit-aktiva-api/
- **API base URL:** `https://aktiva.merit.ee/api`

## Authentication

### API key

Connect Merit with an API ID plus API key generated in Settings > API Settings.

### Credentials

- **API Key:** `apiKey` · required
- **API ID:** `apiId` · required · The API ID generated in Merit Aktiva Settings > API Settings.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.merit.ee/connecting-robots/reference-manual/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Credit Invoice](actions/create-credit-invoice.md) | `POST v1/sendinvoice` | [docs](https://api.merit.ee/connecting-robots/reference-manual/sales-invoices/create-credit-invoice/) |
| [Create Customer](actions/create-customer.md) | `POST v2/sendcustomer` | [docs](https://api.merit.ee/connecting-robots/reference-manual/customers/create-customer/) |
| [Create Customer Group](actions/create-customer-group.md) | `POST v2/sendcustomergroup` | [docs](https://api.merit.ee/connecting-robots/reference-manual/customers/create-customergroup/) |
| [Create Invoice From Sales Offer](actions/create-invoice-from-sales-offer.md) | `POST v2/offer2inv` | [docs](https://api.merit.ee/connecting-robots/reference-manual/sales-offers/create-invoice-from-salesoffer/) |
| [Create Item](actions/create-item.md) | `POST v2/senditems` | [docs](https://api.merit.ee/connecting-robots/reference-manual/items/add-items/) |
| [Create Item Group](actions/create-item-group.md) | `POST v2/senditemgroups` | [docs](https://api.merit.ee/connecting-robots/reference-manual/items/add-item-groups/) |
| [Create Payment Of Purchase Invoice](actions/create-payment-of-purchase-invoice.md) | `POST v2/sendPaymentV` | [docs](https://api.merit.ee/connecting-robots/reference-manual/payments/payment-of-purchase-invoice/) |
| [Create Payment Of Sales Invoice](actions/create-payment-of-sales-invoice.md) | `POST v2/sendpayment` | [docs](https://api.merit.ee/connecting-robots/reference-manual/payments/create-payment/) |
| [Create Payment Of Sales Offer](actions/create-payment-of-sales-offer.md) | `POST v2/sendPaymentO` | [docs](https://api.merit.ee/connecting-robots/reference-manual/payments/create-payment-of-sales-offer/) |
| [Create Purchase Invoice](actions/create-purchase-invoice.md) | `POST v2/sendpurchinvoice` | [docs](https://api.merit.ee/connecting-robots/reference-manual/purchase-invoices/create-purchase-invoice/) |
| [Create Purchase Invoice Waiting Approval](actions/create-purchase-invoice-waiting-approval.md) | `POST v2/sendpurchorder` | [docs](https://api.merit.ee/connecting-robots/reference-manual/purchase-invoices/create-purchase-order/) |
| [Create Recurring Invoice](actions/create-recurring-invoice.md) | `POST v2/sendperinvoice` | [docs](https://api.merit.ee/connecting-robots/reference-manual/recurring-invoices/create-recurring-invoice/) |
| [Create Sales Invoice](actions/create-sales-invoice.md) | `POST v2/sendinvoice` | [docs](https://api.merit.ee/connecting-robots/reference-manual/sales-invoices/create-sales-invoice/) |
| [Create Sales Offer](actions/create-sales-offer.md) | `POST v2/sendoffer` | [docs](https://api.merit.ee/connecting-robots/reference-manual/sales-offers/create-sales-offer/) |
| [Create Vendor](actions/create-vendor.md) | `POST v2/sendvendor` | [docs](https://api.merit.ee/connecting-robots/reference-manual/vendors/create-vendor/) |
| [Delete Payment](actions/delete-payment.md) | `POST v1/deletepayment` | [docs](https://api.merit.ee/connecting-robots/reference-manual/payments/delete-payment/) |
| [Delete Purchase Invoice](actions/delete-purchase-invoice.md) | `POST v1/deletepurchinvoice` | [docs](https://api.merit.ee/connecting-robots/reference-manual/purchase-invoices/delete-purchase-invoice/) |
| [Delete Sales Invoice](actions/delete-sales-invoice.md) | `POST v1/deleteinvoice` | [docs](https://api.merit.ee/connecting-robots/reference-manual/sales-invoices/delete-invoice/) |
| [Get Purchase Invoice Details](actions/get-purchase-invoice-details.md) | `POST v2/getpurchorder` | [docs](https://api.merit.ee/connecting-robots/reference-manual/purchase-invoices/get-purchase-invoice-details/) |
| [Get Recurring Invoice Details](actions/get-recurring-invoice-details.md) | `POST v2/getperinvoice` | [docs](https://api.merit.ee/connecting-robots/reference-manual/recurring-invoices/get-recurring-invoice-details/) |
| [Get Sales Invoice Details](actions/get-sales-invoice-details.md) | `POST v2/getinvoice` | [docs](https://api.merit.ee/connecting-robots/reference-manual/sales-invoices/get-invoice-details/) |
| [Get Sales Invoice PDF](actions/get-sales-invoice-pdf.md) | `POST v2/getsalesinvpdf` | [docs](https://api.merit.ee/connecting-robots/reference-manual/sales-invoices/create-sales-invoice/get-sales-invoice-pdf/) |
| [Get Sales Offer Details](actions/get-sales-offer-details.md) | `POST v2/getoffer` | [docs](https://api.merit.ee/connecting-robots/reference-manual/sales-offers/get-sales-offer-details/) |
| [List Customers](actions/list-customers.md) | `POST v1/getcustomers` | [docs](https://api.merit.ee/connecting-robots/reference-manual/customers/get-customer-list/) |
| [List Item Groups](actions/list-item-groups.md) | `POST v2/getitemgroups` | [docs](https://api.merit.ee/connecting-robots/reference-manual/items/get-item-groups/) |
| [List Items](actions/list-items.md) | `POST v1/getitems` | [docs](https://api.merit.ee/connecting-robots/reference-manual/items/items-list/) |
| [List Payment Types](actions/list-payment-types.md) | `POST v2/getpaymenttypes` | [docs](https://api.merit.ee/connecting-robots/reference-manual/payments/list-of-payment-types/) |
| [List Payments](actions/list-payments.md) | `POST v2/getpayments` | [docs](https://api.merit.ee/connecting-robots/reference-manual/payments/list-of-payments/) |
| [List Purchase Invoices](actions/list-purchase-invoices.md) | `POST v2/getpurchorders` | [docs](https://api.merit.ee/connecting-robots/reference-manual/purchase-invoices/get-list-of-purchase-invoices/) |
| [List Recurring Invoices](actions/list-recurring-invoices.md) | `POST v2/getperinvoices` | [docs](https://api.merit.ee/connecting-robots/reference-manual/recurring-invoices/get-list-of-recurring-invoices/) |
| [List Sales Invoices](actions/list-sales-invoices.md) | `POST v2/getinvoices` | [docs](https://api.merit.ee/connecting-robots/reference-manual/sales-invoices/get-list-of-invoices/) |
| [List Sales Offers](actions/list-sales-offers.md) | `POST v2/getoffers` | [docs](https://api.merit.ee/connecting-robots/reference-manual/sales-offers/get-list-of-sales-offers/) |
| [List Taxes](actions/list-taxes.md) | `POST v1/gettaxes` | [docs](https://api.merit.ee/connecting-robots/reference-manual/tax-list/) |
| [List Vendors](actions/list-vendors.md) | `POST v1/getvendors` | [docs](https://api.merit.ee/connecting-robots/reference-manual/vendors/get-vendor-list/) |
| [Update Customer](actions/update-customer.md) | `POST v1/updatecustomer` | [docs](https://api.merit.ee/connecting-robots/reference-manual/customers/update-customer/) |
| [Update Item](actions/update-item.md) | `POST v1/updateitem` | [docs](https://api.merit.ee/connecting-robots/reference-manual/items/update-item/) |
| [Update Sales Offer](actions/update-sales-offer.md) | `POST v2/updateoffer` | [docs](https://api.merit.ee/connecting-robots/reference-manual/sales-offers/update-sales-offer/) |
