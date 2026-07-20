# BILL Payables & Receivables: Native API Reference

A consolidated summary of BILL Payables & Receivables's API configuration and 19 documented operations.

- **API base URL:** `https://api.bill.com/api/v2`

## Authentication

### Custom

### Credentials

- **Developer Key:** `devKey` · optional
- **Username:** `username` · optional
- **Password:** `password` · optional
- **Organization Id:** `organizationId` · optional

Send these headers with each API request:

```http
devKey: <devKey>
sessionId: <custom.sessionId>
```

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Shared parameters:

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `devKey` | body | `string` | no |
| `sessionId` | body | `string` | no |

Responses from this API use JSON.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Approve Bill](actions/approve-bill.md) | `POST Approve.json` |  |
| [Authenticate](actions/authenticate.md) | `POST Login.json` |  |
| [Create Record](actions/create-record.md) | `POST Crud/Create/:recordType` | [docs](https://developer.bill.com/v2/reference/ap-vendortransactions-createpurchaseorder) |
| [Update Record](actions/create-record-copy.md) | `POST Crud/Update/:recordType` | [docs](https://developer.bill.com/v2/reference/ap-vendormgmt-updatevendor) |
| [Create Vendor](actions/create-vendor.md) | `POST Crud/Create/Vendor.json` | [docs](https://developer.bill.com/v2/reference/ap-vendormgmt-createvendor) |
| [Get Bill](actions/get-bill.md) | `POST Crud/Read/Bill.json` | [docs](https://developer.bill.com/v2/reference/ap-vendortransactions-readbill) |
| [List Approvers Assigned to a Bill](actions/list-bill-approvers.md) | `POST ListApprovers.json` | [docs](https://developer.bill.com/v2/reference/ap-approvals-listapprovers) |
| [List Bill Credits](actions/list-bill-credits.md) | `POST List/BillCredit.json` | [docs](https://developer.bill.com/v2/reference/ap-vendortransactions-listbillcredit) |
| [List Bills](actions/list-bills.md) | `POST List/Bill.json` | [docs](https://developer.bill.com/v2/reference/ap-vendortransactions-listbill) |
| [List Charts of Accounts](actions/list-charts-of-accounts.md) | `POST List/ChartOfAccount.json` | [docs](https://developer.bill.com/v2/reference/org-accounts-listchartofaccount) |
| [List Customers](actions/list-customers.md) | `POST List/Customer.json` | [docs](https://developer.bill.com/v2/reference/ar-customermgmt-listcustomer) |
| [List Invoices](actions/list-invoices.md) | `POST List/Invoice.json` | [docs](https://developer.bill.com/v2/reference/ar-customertransactions-listinvoice) |
| [List Items](actions/list-items.md) | `POST List/Item.json` | [docs](https://developer.bill.com/v2/reference/org-accounts-listitem) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `POST List/PurchaseOrder.json` | [docs](https://developer.bill.com/v2/reference/ap-vendortransactions-listpurchaseorders) |
| [List Sent Payments](actions/list-sent-payments.md) | `POST List/SentPay.json` | [docs](https://developer.bill.com/v2/reference/ap-vendortransactions-listsentpay) |
| [List Users](actions/list-users.md) | `POST List/User.json` | [docs](https://developer.bill.com/v2/reference/org-basic-listuser) |
| [List Vendor Credits](actions/list-vendor-credits.md) | `POST List/VendorCredit.json` | [docs](https://developer.bill.com/v2/reference/ap-vendortransactions-listvendorcredit) |
| [List Vendors](actions/list-vendors.md) | `POST List/Vendor.json` | [docs](https://developer.bill.com/v2/reference/ap-vendormgmt-listvendor) |
| [Update Vendor](actions/update-vendor.md) | `POST Crud/Update/Vendor.json` | [docs](https://developer.bill.com/v2/reference/ap-vendormgmt-updatevendor) |
