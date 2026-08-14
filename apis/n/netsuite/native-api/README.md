# NetSuite - Advanced: Native API Reference

A consolidated summary of NetSuite - Advanced's API configuration and 181 documented operations, with links to official documentation.

- **Official docs:** https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/
- **REST base URL:** `https://{accountId}.suitetalk.api.netsuite.com`

## Authentication

### OAuth 1.0

### Credentials

- **Consumer Key:** `consumerKey` · required
- **Consumer Secret:** `consumerSecret` · required
- **Access Token:** `accessToken` · required
- **Token Secret:** `tokenSecret` · required
- **Realm:** `realm` · optional
- **Deployment Access Token:** `deploymentAccessToken` · optional
- **Deployment Token Secret:** `deploymentTokenSecret` · optional

OAuth 1.0a signs every request with the consumer key and secret plus the access token and token secret. Use an OAuth 1.0a client library to construct the `Authorization` header; the signature depends on the HTTP method, URL, and request parameters and should not be assembled as a static token.

## API conventions

### REST

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

- **REST:** Use `limit` in the request body to set the page size (default 1000; accepted range 1–1000). Use `offset` in the request body to choose the result range.

## Filtering

- **REST:** Send filters in the request body. Supported operators: `eq`, `gt`, `gte`, `lt`, `lte`, `ne`.

## Sorting

- **REST:** Send sorting in the request body. Only one sort field is accepted.

## Retry behavior

- **REST:** Wait 5000 ms before the first retry. Stop after 5 attempts. Multiply the delay by 2 after each failed attempt.
- **Internal:** Wait 5000 ms before the first retry. Stop after 5 attempts. Multiply the delay by 3 after each failed attempt.

## Endpoints (181 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Assembly Item](actions/create-assembly-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Cash Refund](actions/create-cash-refund.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Cash Sale](actions/create-cash-sale.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Contact](actions/create-contact.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/contact.html) |
| [Create Credit Memo](actions/create-credit-memo.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Custom Record](actions/create-custom-record.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Customer](actions/create-customer.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/customer.html) |
| [Create Customer Deposit](actions/create-customer-deposit.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Customer Payment](actions/create-customer-payment.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Customer Refund](actions/create-customer-refund.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Deposit](actions/create-deposit.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Employee](actions/create-employee.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Group Item](actions/create-group-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Inventory Adjustment](actions/create-inventory-adjustment.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Inventory Item](actions/create-inventory-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Invoice](actions/create-invoice.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Item Fulfillment](actions/create-item-fulfillment.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Item Receipt](actions/create-item-receipt.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Location](actions/create-location.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Lot Numbered Assembly Item](actions/create-lot-numbered-assembly-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Lot Numbered Inventory Item](actions/create-lot-numbered-inventory-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Non-Inventory Item](actions/create-non-inventory-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Other Charge Item](actions/create-other-charge-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Project](actions/create-project.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Project Task](actions/create-project-task.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Promotion Code](actions/create-promotion-code.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Purchase Order](actions/create-purchase-order.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Sales Order](actions/create-sales-order.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Serialized Assembly Item](actions/create-serialized-assembly-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Serialized Inventory Item](actions/create-serialized-inventory-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Service Item](actions/create-service-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Shipping Item](actions/create-shipping-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Term](actions/create-term.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Time Bill](actions/create-time-bill.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Vendor](actions/create-vendor.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Create Vendor Return Authorization](actions/create-vendor-return-authorization.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://www.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2020_1/schema/record/vendorreturnauthorization.html) |
| [Create Work Order](actions/create-work-order.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Account](actions/delete-account.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Accounting Period](actions/delete-accounting-period.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Assembly Item](actions/delete-assembly-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Cash Refund](actions/delete-cash-refund.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Cash Sale](actions/delete-cash-sale.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Classification](actions/delete-classification.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Contact](actions/delete-contact.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Credit Memo](actions/delete-credit-memo.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Custom Record](actions/delete-custom-record.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Customer](actions/delete-customer.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Customer Deposit](actions/delete-customer-deposit.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Customer Payment](actions/delete-customer-payment.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Customer Refund](actions/delete-customer-refund.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Employee](actions/delete-employee.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete File](actions/delete-file.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Group Item](actions/delete-group-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Inventory Adjustment](actions/delete-inventory-adjustment.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Inventory Item](actions/delete-inventory-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Invoice](actions/delete-invoice.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Item](actions/delete-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Item Fulfillment](actions/delete-item-fulfillment.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Item Receipt](actions/delete-item-receipt.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Location](actions/delete-location.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Lot Numbered Assembly Item](actions/delete-lot-numbered-assembly-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Lot Numbered Inventory Item](actions/delete-lot-numbered-inventory-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Non-Inventory Item](actions/delete-non-inventory-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Other Charge Item](actions/delete-other-charge-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Project](actions/delete-project.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Project Task](actions/delete-project-task.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Promotion Code](actions/delete-promotion-code.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Purchase Order](actions/delete-purchase-order.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Sales Order](actions/delete-sales-order.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Serialized Assembly Item](actions/delete-serialized-assembly-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Serialized Inventory Item](actions/delete-serialized-inventory-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Service Item](actions/delete-service-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Shipping Item](actions/delete-shipping-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Term](actions/delete-term.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Time Bill](actions/delete-time-bill.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Transfer Order](actions/delete-transfer-order.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Vendor](actions/delete-vendor.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Vendor Bill](actions/delete-vendor-bill.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Delete Vendor Credit](actions/delete-vendor-credit.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Execute Custom Code](actions/execute-custom-code.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/article_163726005075.html#subsect_164988373340) |
| [List Items](actions/get-assembly-items.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/account.html) |
| [Get Restlet](actions/get-restlet.md) | `GET https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Search using Saved Search](actions/get-saved-search.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_156257770590.html) |
| [List Accounting Periods](actions/list-accounting-periods.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/accountingperiod.html) |
| [List Accounts](actions/list-accounts.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/account.html) |
| [List Assembly Items](actions/list-assembly-items.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/assemblyitem.html) |
| [List Bin Numbers](actions/list-bin-numbers.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/bin.html) |
| [List Cash Refunds](actions/list-cash-refunds.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/cashrefund.html) |
| [List Cash Sales](actions/list-cash-sales.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/cashsale.html) |
| [List Classifications](actions/list-classifications.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/classification.html) |
| [List Contacts](actions/list-contacts.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/contact.html) |
| [List Credit Memos](actions/list-credit-memos.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/creditmemo.html) |
| [List Custom Records](actions/list-custom-records.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/account.html) |
| [List Customer Deposits](actions/list-customer-deposits.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/customerdeposit.html) |
| [List Customer Payments](actions/list-customer-payments.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/customerpayment.html) |
| [List Customer Refunds](actions/list-customer-refunds.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://www.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2017_1/script/record/customerrefund.html) |
| [List Customers](actions/list-customers.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/customer.html) |
| [List Departments](actions/list-departments.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/department.html) |
| [List Employees](actions/list-employees.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/employee.html) |
| [List Files](actions/list-files.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/file.html) |
| [List Group Items](actions/list-group-items.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/itemgroup.html) |
| [List Inbound Shipments](actions/list-inbound-shipments.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/inboundshipment.html) |
| [List Inventory Adjustments](actions/list-inventory-adjustments.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://www.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2018_1/script/record/inventoryadjustment.html) |
| [List Inventory Items](actions/list-inventory-items.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/inventoryitem.html) |
| [List Inventory Numbers](actions/list-inventory-numbers.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/inventorynumber.html) |
| [List Invoices](actions/list-invoices.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/invoice.html) |
| [List Item Fulfillments](actions/list-item-fulfillments.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/itemfulfillment.html) |
| [List Item Receipts](actions/list-item-receipts.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/itemreceipt.html) |
| [List Locations](actions/list-locations.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/location.html) |
| [List Lot Numbered Assembly Items](actions/list-lot-numbered-assembly-items.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/lotnumberedassemblyitem.html) |
| [List Lot Numbered Inventory Items](actions/list-lot-numbered-inventory-items.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/lotnumberedinventoryitem.html) |
| [List Non-Inventory Items](actions/list-non-inventory-items.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/noninventoryitem.html) |
| [List Opportunities](actions/list-opportunities.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/opportunity.html) |
| [List Other Charge Items](actions/list-other-charge-items.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/otherchargeitem.html) |
| [List Payment Methods](actions/list-payment-methods.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/paymentmethod.html) |
| [List Project Tasks](actions/list-project-tasks.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/projecttask.html) |
| [List Projects](actions/list-projects.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/job.html) |
| [List Promotion Codes](actions/list-promotion-codes.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/promotioncode.html) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/partner.html) |
| [List Record Fields](actions/list-record-fields.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [List Return Authorizations](actions/list-return-authorizations.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://www.netsuite.com/portal/home.shtml) |
| [List Sales Orders](actions/list-sales-orders.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://www.netsuite.com/portal/home.shtml) |
| [List Serialized Assembly Items](actions/list-serialized-assembly-items.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/serializedassemblyitem.html) |
| [List Serialized Inventory Items](actions/list-serialized-inventory-items.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/serializedinventoryitem.html) |
| [List Service Items](actions/list-service-items.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/serviceitem.html) |
| [List Shipping Items](actions/list-shipping-items.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/shipitem.html) |
| [List States](actions/list-states.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/schema/record/state.html) |
| [List Subsidiaries](actions/list-subsidiaries.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/subsidiary.html) |
| [List Tasks](actions/list-tasks.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/task.html) |
| [List Terms](actions/list-terms.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/term.html) |
| [List Time Bills](actions/list-time-bills.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/timebill.html) |
| [List Transfer Orders](actions/list-transfer-orders.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://www.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2017_1/script/record/transferorder.html) |
| [List Vendor Bills](actions/list-vendor-bills.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/vendorbill.html) |
| [List Vendor Credits](actions/list-vendor-credits.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/vendorcredit.html) |
| [List Vendor Return Authorizations](actions/list-vendor-return-authorizations.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://www.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2017_2/script/record/vendorreturnauthorization.html) |
| [List Vendors](actions/list-vendors.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/vendor.html) |
| [List Work Orders](actions/list-work-orders.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://www.netsuite.com/portal/home.shtml) |
| [Get Item Fulfillment](actions/new-action1.md) | `GET /services/rest/record/v1/ItemFulfillment/:id` | [docs](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_161425629582.html) |
| [Update Account](actions/update-account.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Assembly Item](actions/update-assembly-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Cash Refund](actions/update-cash-refund.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Cash Sale](actions/update-cash-sale.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Classification](actions/update-classification.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Contact](actions/update-contact.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/contact.html) |
| [Update Credit Memo](actions/update-credit-memo.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Custom Record](actions/update-custom-record.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Customer](actions/update-customer.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` | [docs](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/customer.html) |
| [Update Customer Deposit](actions/update-customer-deposit.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Customer Payment](actions/update-customer-payment.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Customer Refund](actions/update-customer-refund.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Employee](actions/update-employee.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Group Item](actions/update-group-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Inventory Adjustment](actions/update-inventory-adjustment.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Inventory Item](actions/update-inventory-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Invoice](actions/update-invoice.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Item Fulfillments](actions/update-item-fulfillments.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Item Receipt](actions/update-item-receipt.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Location](actions/update-location.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Lot Numbered Assembly Item](actions/update-lot-numbered-assembly-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Lot Numbered Inventory Item](actions/update-lot-numbered-inventory-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Non-Inventory Item](actions/update-non-inventory-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Term](actions/update-other-change-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Other Charge Item](actions/update-other-charge-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Project](actions/update-project.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Project Task](actions/update-project-task.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Promotion Code](actions/update-promotion-code.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Purchase Order](actions/update-purchase-order.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Return Authorization](actions/update-return-authorization.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Sales Order](actions/update-sales-order.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Serialized Assembly Item](actions/update-serialized-assembly-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Serialized Inventory Item](actions/update-serialized-inventory-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Service Item](actions/update-service-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Shipping Item](actions/update-shipping-item.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Time Bill](actions/update-time-bill.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Transfer Order](actions/update-transfer-order.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Vendor](actions/update-vendor.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Vendor Bill](actions/update-vendor-bill.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Vendor Credit](actions/update-vendor-credit.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Vendor Return Authorization](actions/update-vendor-return-authorization.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
| [Update Work Order](actions/update-work-order.md) | `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` |  |
