# Viewpoint Spectrum: Native API Reference

A consolidated summary of Viewpoint Spectrum's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://help.trimble.com/en/spectrum/spectrum/api-web-services/api-web-services
- **API base URL:** `{url}:8482/`

## Authentication

### Custom

### Credentials

- **URL:** `url` · optional · Company URL, such as https://my.company.com
- **Company ID:** `companyID` · optional · Company name, as shown in the Viewpoint Spectrum interface dropdown menu.
- **Authorization ID:** `authorizationID` · optional

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `$limit` in the query string to set the page size (default 25; accepted range 1–500). Use `$skip` in the query string as the record offset.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Cash Receipts](actions/add-cash-receipts.md) | `POST /ws/AddCash_Receipts` |  |
| [Add Cash Receipts (SOAP)](actions/add-cash-receipts-soap.md) | `POST /ws/AddCash_Receipts` |  |
| [Create AR Customer Invoice Multi-Line](actions/create-ar-customer-invoice-multi-line.md) | `POST customer/invoice` |  |
| [Create Customer](actions/create-customer.md) | `POST ws/AddCustomer` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-receivable-services/add-customer) |
| [Create Customer Invoice](actions/create-customer-invoice.md) | `POST ws/AddARInvoice` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/add-vendor-invoices) |
| [Create Purchase Order](actions/create-purchase-order.md) | `POST purchaseOrders` | [docs](https://help.trimble.com/doc/spectrum/spectrum/api-web-services/list-of-web-services/purchase-order-services/purchase-order-batch) |
| [Create Vendor](actions/create-vendor.md) | `POST ws/AddVendor` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/add-vendor) |
| [Create Vendor Invoice](actions/create-vendor-invoice.md) | `POST ws/AddAPInvoice` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/add-vendor-invoices) |
| [Create Vendor Invoice Multi-Line](actions/create-vendor-invoice-multi-line.md) | `POST vendor/invoice` |  |
| [Create Vendor (SOAP)](actions/create-vendor-soap.md) | `POST ws/AddVendor` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-receivable-services/add-customer) |
| [Create Work Orders](actions/create-work-orders.md) | `POST ws/WorkOrderHeader` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/add-vendor-invoices) |
| [Get Customers](actions/get-customers.md) | `POST ws/GetCustomers` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-receivable-services/get-customers) |
| [List Customers](actions/list-customers.md) | `POST ws/GetCustomers` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-receivable-services/get-customers) |
| [List Vendors](actions/list-vendors.md) | `GET vendors/{{credentials.companyID}}` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/get-vendors) |
| [Update Customer](actions/update-customer.md) | `POST ws/AddCustomer` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-receivable-services/update-customer) |
| [Update Vendor](actions/update-vendor.md) | `POST ws/UpdateVendor` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/update-vendor) |
| [Update Vendor (SOAP)](actions/update-vendor-soap.md) | `POST ws/UpdateVendor` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/update-vendor) |
| [Upsert Customer Bill-To](actions/upsert-customer-bill-to.md) | `POST ws/CustomerBillto` |  |
