# NetSuite - Basic: Native API Reference

A consolidated summary of NetSuite - Basic's API configuration and 99 documented operations, with links to official documentation.

- **Official docs:** https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/chapter_1540391670.html
- **API base URL:** `https://{accountDomain}.suitetalk.api.netsuite.com/services/rest`

## Authentication

### OAuth 2.0

Connect with NetSuite OAuth 2.0 Authorization Code Grant for SuiteTalk REST Web Services.

### Credentials

- **Account ID:** `accountId` · required · Enter the official NetSuite Account ID from Company Information, for example 123456 for production or 123456_SB1 for sandbox.
- **Consumer Key / Client ID:** `clientId` · required · Paste the Consumer Key / Client ID shown by NetSuite after saving the OAuth 2.0 integration record.
- **Consumer Secret / Client Secret:** `clientSecret` · required · Paste the Consumer Secret / Client Secret shown by NetSuite after saving the OAuth 2.0 integration record. NetSuite only shows this value once.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://{{credentials.accountDomain}}.app.netsuite.com/app/login/oauth2/authorize.nl to approve access.
2. Exchange the returned authorization code with a POST request to https://{{credentials.accountDomain}}.suitetalk.api.netsuite.com/services/rest/auth/oauth2/v1/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `rest_webservices`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://{{credentials.accountDomain}}.suitetalk.api.netsuite.com/services/rest/auth/oauth2/v1/token.

[Official authentication documentation](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/chapter_157769826287.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `items`.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (99 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | `POST /record/v1/account` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/account) |
| [Create Classification](actions/create-classification.md) | `POST /record/v1/classification` | [docs](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/chapter_1558962745.html) |
| [Create Contact](actions/create-contact.md) | `POST /record/v1/contact` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/contact) |
| [Create Customer](actions/create-customer.md) | `POST /record/v1/customer` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/customer) |
| [Create Employee](actions/create-employee.md) | `POST /record/v1/employee` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/employee) |
| [Create Location](actions/create-location.md) | `POST /record/v1/location` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/location) |
| [Create Purchase Order](actions/create-purchase-order.md) | `POST /record/v1/purchaseOrder` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/purchaseOrder) |
| [Create Term](actions/create-term.md) | `POST /record/v1/term` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/term) |
| [Create Time Bill](actions/create-time-bill.md) | `POST /record/v1/timeBill` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/timeBill) |
| [Create Vendor](actions/create-vendor.md) | `POST /record/v1/vendor` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/vendor) |
| [Create Vendor Bill](actions/create-vendor-bill.md) | `POST /record/v1/vendorBill` | [docs](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/chapter_1558962745.html) |
| [Delete Account](actions/delete-account.md) | `DELETE /record/v1/account/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/account) |
| [Delete Classification](actions/delete-classification.md) | `DELETE /record/v1/classification/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/classification) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /record/v1/contact/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/contact) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /record/v1/customer/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/customer) |
| [Delete Employee](actions/delete-employee.md) | `DELETE /record/v1/employee/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/employee) |
| [Delete Location](actions/delete-location.md) | `DELETE /record/v1/location/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/location) |
| [Delete Purchase Order](actions/delete-purchase-order.md) | `DELETE /record/v1/purchaseOrder/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/purchaseOrder) |
| [Delete Term](actions/delete-term.md) | `DELETE /record/v1/term/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/term) |
| [Delete Time Bill](actions/delete-time-bill.md) | `DELETE /record/v1/timeBill/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/timeBill) |
| [Delete Vendor](actions/delete-vendor.md) | `DELETE /record/v1/vendor/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/vendor) |
| [Delete Vendor Bill](actions/delete-vendor-bill.md) | `DELETE /record/v1/vendorBill/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/vendorBill) |
| [Get Contact](actions/get-contact.md) | `GET /record/v1/contact/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/contact) |
| [Get Customer](actions/get-customer.md) | `GET /record/v1/customer/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/customer) |
| [Get Estimate](actions/get-estimate.md) | `GET /record/v1/estimate/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/estimate) |
| [Get Inventory Item](actions/get-inventory-item.md) | `GET /record/v1/inventoryItem/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/inventoryItem) |
| [Get Invoice](actions/get-invoice.md) | `GET /record/v1/invoice/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/invoice) |
| [Get Non-Inventory Sale Item](actions/get-non-inventory-sale-item.md) | `GET /record/v1/nonInventorySaleItem/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/nonInventorySaleItem) |
| [Get Purchase Order](actions/get-purchase-order.md) | `GET /record/v1/purchaseOrder/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/purchaseOrder) |
| [Get Record Fields](actions/get-record-fields.md) | `GET /record/v1/metadata-catalog/:recordType` | [docs](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_1540810174.html) |
| [Get Record Types](actions/get-record-types.md) | `GET /record/v1/metadata-catalog` | [docs](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_1540810174.html) |
| [Get Sales Order](actions/get-sales-order.md) | `GET /record/v1/salesOrder/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/salesOrder) |
| [Get Vendor](actions/get-vendor.md) | `GET /record/v1/vendor/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/vendor) |
| [Get Vendor Bill](actions/get-vendor-bill.md) | `GET /record/v1/vendorBill/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/vendorBill) |
| [List Accounting Periods](actions/list-accounting-periods.md) | `GET /record/v1/accountingPeriod` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/accountingPeriod) |
| [List Accounts](actions/list-accounts.md) | `GET /record/v1/account` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/account) |
| [List Assembly Items](actions/list-assembly-items.md) | `GET /record/v1/assemblyItem` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/assemblyItem) |
| [List Bin Numbers](actions/list-bin-numbers.md) | `GET /record/v1/bin` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/bin) |
| [List Cash Refunds](actions/list-cash-refunds.md) | `GET /record/v1/cashRefund` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/cashRefund) |
| [List Cash Sales](actions/list-cash-sales.md) | `GET /record/v1/cashSale` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/cashSale) |
| [List Classifications](actions/list-classifications.md) | `GET /record/v1/classification` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/classification) |
| [List Contacts](actions/list-contacts.md) | `GET /record/v1/contact` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/contact) |
| [List Credit Memos](actions/list-credit-memos.md) | `GET /record/v1/creditMemo` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/creditMemo) |
| [List Custom Records](actions/list-custom-records.md) | `GET /record/v1/:recordType` | [docs](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/chapter_1540810168.html) |
| [List Customer Deposits](actions/list-customer-deposits.md) | `GET /record/v1/customerDeposit` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/customerDeposit) |
| [List Customer Payments](actions/list-customer-payments.md) | `GET /record/v1/customerPayment` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/customerPayment) |
| [List Customer Refunds](actions/list-customer-refunds.md) | `GET /record/v1/customerRefund` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/customerRefund) |
| [List Customers](actions/list-customers.md) | `GET /record/v1/customer` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/customer) |
| [List Departments](actions/list-departments.md) | `GET /record/v1/department` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/department) |
| [List Employees](actions/list-employees.md) | `GET /record/v1/employee` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/employee) |
| [List Estimates](actions/list-estimates.md) | `GET /record/v1/estimate` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/estimate) |
| [List Group Items](actions/list-group-items.md) | `GET /record/v1/itemGroup` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/itemGroup) |
| [List Inbound Shipments](actions/list-inbound-shipments.md) | `GET /record/v1/inboundShipment` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/inboundShipment) |
| [List Inventory Adjustments](actions/list-inventory-adjustments.md) | `GET /record/v1/inventoryAdjustment` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/inventoryAdjustment) |
| [List Inventory Items](actions/list-inventory-items.md) | `GET /record/v1/inventoryItem` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/inventoryItem) |
| [List Inventory Numbers](actions/list-inventory-numbers.md) | `GET /record/v1/inventoryNumber` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/inventoryNumber) |
| [List Invoices](actions/list-invoices.md) | `GET /record/v1/invoice` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/invoice) |
| [List Item Fulfillments](actions/list-item-fulfillments.md) | `GET /record/v1/itemFulfillment` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/itemFulfillment) |
| [List Item Receipts](actions/list-item-receipts.md) | `GET /record/v1/itemReceipt` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/itemReceipt) |
| [List Locations](actions/list-locations.md) | `GET /record/v1/location` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/location) |
| [List Lot Numbered Assembly Items](actions/list-lot-numbered-assembly-items.md) | `GET /record/v1/lotNumberedAssemblyItem` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/lotNumberedAssemblyItem) |
| [List Lot Numbered Inventory Items](actions/list-lot-numbered-inventory-items.md) | `GET /record/v1/lotNumberedInventoryItem` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/lotNumberedInventoryItem) |
| [List Non-Inventory Items](actions/list-non-inventory-items.md) | `GET /record/v1/nonInventorySaleItem` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/nonInventorySaleItem) |
| [List Non-Inventory Sale Items](actions/list-non-inventory-sale-items.md) | `GET /record/v1/nonInventorySaleItem` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/nonInventorySaleItem) |
| [List Opportunities](actions/list-opportunities.md) | `GET /record/v1/opportunity` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/opportunity) |
| [List Other Charge Items](actions/list-other-charge-items.md) | `GET /record/v1/otherChargeSaleItem` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/otherChargeSaleItem) |
| [List Payment Methods](actions/list-payment-methods.md) | `GET /record/v1/paymentMethod` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/paymentMethod) |
| [List Promotion Codes](actions/list-promotion-codes.md) | `GET /record/v1/promotionCode` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/promotionCode) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `GET /record/v1/purchaseOrder` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/purchaseOrder) |
| [List Record Fields](actions/list-record-fields.md) | `GET /record/v1/metadata-catalog/:recordType` | [docs](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/chapter_1540810168.html) |
| [List Return Authorizations](actions/list-return-authorizations.md) | `GET /record/v1/returnAuthorization` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/returnAuthorization) |
| [List Sales Orders](actions/list-sales-orders.md) | `GET /record/v1/salesOrder` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/salesOrder) |
| [List Serialized Assembly Items](actions/list-serialized-assembly-items.md) | `GET /record/v1/serializedAssemblyItem` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/serializedAssemblyItem) |
| [List Serialized Inventory Items](actions/list-serialized-inventory-items.md) | `GET /record/v1/serializedInventoryItem` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/serializedInventoryItem) |
| [List Service Items](actions/list-service-items.md) | `GET /record/v1/serviceSaleItem` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/serviceSaleItem) |
| [List Shipping Items](actions/list-shipping-items.md) | `GET /record/v1/shipItem` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/shipItem) |
| [List Subsidiaries](actions/list-subsidiaries.md) | `GET /record/v1/subsidiary` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/subsidiary) |
| [List Tasks](actions/list-tasks.md) | `GET /record/v1/task` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/task) |
| [List Terms](actions/list-terms.md) | `GET /record/v1/term` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/term) |
| [List Time Bills](actions/list-time-bills.md) | `GET /record/v1/timeBill` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/timeBill) |
| [List Transfer Orders](actions/list-transfer-orders.md) | `GET /record/v1/transferOrder` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/transferOrder) |
| [List Vendor Bills](actions/list-vendor-bills.md) | `GET /record/v1/vendorBill` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/vendorBill) |
| [List Vendor Credits](actions/list-vendor-credits.md) | `GET /record/v1/vendorCredit` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/vendorCredit) |
| [List Vendor Return Authorizations](actions/list-vendor-return-authorizations.md) | `GET /record/v1/vendorReturnAuthorization` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/vendorReturnAuthorization) |
| [List Vendors](actions/list-vendors.md) | `GET /record/v1/vendor` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/vendor) |
| [List Work Orders](actions/list-work-orders.md) | `GET /record/v1/workOrder` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/workOrder) |
| [Search using SuiteQL](actions/search-using-suite-ql.md) | `POST /query/v1/suiteql` | [docs](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_157909186990.html) |
| [Test Connection](actions/test-connection.md) | `GET /record/v1/account` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/account) |
| [Update Account](actions/update-account.md) | `PATCH /record/v1/account/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/account) |
| [Update Classification](actions/update-classification.md) | `PATCH /record/v1/classification/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/classification) |
| [Update Contact](actions/update-contact.md) | `PATCH /record/v1/contact/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/contact) |
| [Update Customer](actions/update-customer.md) | `PATCH /record/v1/customer/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/customer) |
| [Update Employee](actions/update-employee.md) | `PATCH /record/v1/employee/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/employee) |
| [Update Location](actions/update-location.md) | `PATCH /record/v1/location/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/location) |
| [Update Purchase Order](actions/update-purchase-order.md) | `PATCH /record/v1/purchaseOrder/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/purchaseOrder) |
| [Update Term](actions/update-term.md) | `PATCH /record/v1/term/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/term) |
| [Update Time Bill](actions/update-time-bill.md) | `PATCH /record/v1/timeBill/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/timeBill) |
| [Update Vendor](actions/update-vendor.md) | `PATCH /record/v1/vendor/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/vendor) |
| [Update Vendor Bill](actions/update-vendor-bill.md) | `PATCH /record/v1/vendorBill/:id` | [docs](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/vendorBill) |
