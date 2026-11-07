# Viewpoint Spectrum: Native API Reference

A consolidated summary of Viewpoint Spectrum's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://help.trimble.com/en/spectrum/spectrum/api-web-services/api-web-services
- **REST base URL:** `{url}:8482/`
- **RAW Text base URL:** `{url}:8482/`

## Authentication

### Basic Authentication

### Credentials

- **URL:** `url` · optional · Company URL, such as https://my.company.com
- **Company ID:** `companyID` · optional · Company name, as shown in the Viewpoint Spectrum interface dropdown menu.
- **Authorization ID:** `authorizationID` · optional

## API conventions

### REST

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

### RAW Text

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use plain text.

## Pagination

- **REST:** Use `$limit` in the query string to set the page size (default 25; accepted range 1–500). Use `$skip` in the query string as the record offset.

## Endpoints (24 documented)

| Operation | API | Method & path | Vendor docs |
| --- | --- | --- | --- |
| [Add Cash Receipts](actions/add-cash-receipts.md) | REST | `POST /ws/AddCash_Receipts` |  |
| [Add Cash Receipts (SOAP)](actions/add-cash-receipts-soap.md) | REST | `POST /ws/AddCash_Receipts` |  |
| [Add G/L Journal Entry](actions/add-gl-journal-entry.md) | REST | `POST ws/AddGLTrans` | [docs](https://help.trimble.com/doc/spectrum/spectrum/api-web-services/list-of-web-services/general-ledger-services/add-gl-journal-entries) |
| [Add Work Order Site Address](actions/add-work-order-site-address.md) | REST | `POST ws/AddWOSiteAddress` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/add-vendor-invoices) |
| [Create AR Customer Invoice Multi-Line](actions/create-ar-customer-invoice-multi-line.md) | REST | `POST customer/invoice` | [docs](https://help.trimble.com/doc/spectrum/spectrum/api-web-services/list-of-web-services/accounts-receivable-services/multi-line-customer-invoice) |
| [Create Customer](actions/create-customer.md) | REST | `POST ws/AddCustomer` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-receivable-services/add-customer) |
| [Create Customer Invoice](actions/create-customer-invoice.md) | REST | `POST ws/AddARInvoice` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/add-vendor-invoices) |
| [Create Purchase Order](actions/create-purchase-order.md) | REST | `POST purchaseOrders` | [docs](https://help.trimble.com/doc/spectrum/spectrum/api-web-services/list-of-web-services/purchase-order-services/purchase-order-batch) |
| [Create Vendor](actions/create-vendor.md) | REST | `POST ws/AddVendor` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/add-vendor) |
| [Create Vendor Invoice](actions/create-vendor-invoice.md) | REST | `POST ws/AddAPInvoice` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/add-vendor-invoices) |
| [Create Vendor Invoice Multi-Line](actions/create-vendor-invoice-multi-line.md) | REST | `POST vendor/invoice` |  |
| [Create Vendor Invoice (SOAP)](actions/create-vendor-invoice-soap.md) | REST | `POST ws/AddAPInvoice` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-receivable-services/add-customer) |
| [Create Vendor (SOAP)](actions/create-vendor-soap.md) | REST | `POST ws/AddVendor` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-receivable-services/add-customer) |
| [Create Work Orders](actions/create-work-orders.md) | REST | `POST ws/WorkOrderHeader` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/add-vendor-invoices) |
| [Get Customers](actions/get-customers.md) | REST | `POST ws/GetCustomers` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-receivable-services/get-customers) |
| [Get WSDL](actions/get-wsdl.md) | RAW Text | `GET wsdls/:WSDL` |  |
| [List Customers](actions/list-customers.md) | REST | `POST ws/GetCustomers` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-receivable-services/get-customers) |
| [List Employee](actions/list-employee.md) | REST | `POST ws/GetEmployee.jws` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-receivable-services/get-customers) |
| [List Vendors](actions/list-vendors.md) | REST | `GET vendors/:company` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/get-vendors) |
| [Send Timesheet (SOAP)](actions/send-timesheet-soap.md) | REST | `POST ws/PreTimeCard` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/add-vendor) |
| [Update Customer](actions/update-customer.md) | REST | `POST customer/updatecustomer` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-receivable-services/add-customer) |
| [Update Vendor](actions/update-vendor.md) | REST | `POST ws/UpdateVendor` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/update-vendor) |
| [Update Vendor (SOAP)](actions/update-vendor-soap.md) | REST | `POST ws/UpdateVendor` | [docs](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/update-vendor) |
| [Upsert Customer Bill-To](actions/upsert-customer-bill-to.md) | REST | `POST ws/CustomerBillto` |  |
