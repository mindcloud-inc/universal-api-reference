# QuickBooks Online: Native API Reference

A consolidated summary of QuickBooks Online's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities
- **API base URL:** `https://:quickbooksEnvironment/v3/company/:realmId`

## Authentication

### MindCloud Integration

### Credentials

- **Quickbooks Environment:** `quickbooksEnvironment` · optional

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://appcenter.intuit.com/connect/oauth2 to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth.platform.intuit.com/oauth2/v1/tokens/bearer.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `com.intuit.quickbooks.accounting`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://oauth.platform.intuit.com/oauth2/v1/tokens/bearer.

[Official authentication documentation](https://developer.intuit.com/app/developer/qbo/docs/develop/authentication-and-authorization/oauth-2.0)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON.

## Retry behavior

Wait 10000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | `POST /account` | [docs](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/account#create-an-account) |
| [Create Bill](actions/create-bill.md) | `POST /billpayment` | [docs](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/bill#create-a-bill) |
| [Create Customer](actions/create-customer.md) | `POST /customer` | [docs](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/customer#create-a-customer) |
| [Create Invoice](actions/create-invoice.md) | `POST /invoice` | [docs](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/invoice#create-an-invoice) |
| [Create Item](actions/create-item.md) | `POST /item` | [docs](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/item#create-an-item) |
| [Create Purchase Order](actions/create-purchase-order.md) | `POST /purchaseorder` | [docs](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/purchaseorder#create-a-purchaseorder) |
| [Create Vendor](actions/create-vendor.md) | `POST /vendor` | [docs](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/vendor#create-a-vendor) |
| [Get Account](actions/get-account.md) | `GET /account/:accountId` | [docs](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/account#read-an-account) |
| [Get Bill](actions/get-bill.md) | `GET /bill/:billId` | [docs](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/bill#read-a-bill) |
| [Get Customer](actions/get-customer.md) | `GET /customer/:customerId` | [docs](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/customer#read-a-customer) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoice/:invoiceId` | [docs](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/invoice#read-an-invoice) |
| [Get Item](actions/get-item.md) | `GET /item/:itemId` | [docs](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/item#read-an-item) |
| [Get Profit and Loss](actions/get-profit-and-loss.md) | `GET /reports/ProfitAndLoss` | [docs](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/profitandloss) |
| [Get Purchase Order](actions/get-purchase-order.md) | `GET /purchaseorder/:purchaseOrderId` | [docs](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/purchaseorder#read-a-purchaseorder) |
| [Get Transaction Detail by Account](actions/get-transaction-detail-by-account.md) | `GET /reports/TransactionDetailByAccount` | [docs](https://developer.intuit.com/app/developer/qbo/docs/workflows/run-reports) |
| [Get Transaction List](actions/get-transaction-list.md) | `GET /reports/TransactionList` | [docs](https://developer.intuit.com/app/developer/qbo/docs/workflows/run-reports) |
| [Get Transaction List by Vendor](actions/get-transaction-list-by-vendor.md) | `GET /reports/TransactionListByVendor` | [docs](https://developer.intuit.com/app/developer/qbo/docs/workflows/run-reports) |
| [Get Transaction List with Splits](actions/get-transaction-list-with-splits.md) | `GET /reports/TransactionListWithSplits` | [docs](https://developer.intuit.com/app/developer/qbo/docs/workflows/run-reports) |
| [Get Vendor](actions/get-vendor.md) | `GET /vendor/:vendorId` | [docs](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/vendor#read-a-vendor) |
| [List Accounts](actions/list-accounts.md) | `GET /query` | [docs](https://developer.intuit.com/app/developer/qbo/docs/learn/explore-the-quickbooks-online-api/data-queries) |
| [List Bills](actions/list-bills.md) | `GET /query` | [docs](https://developer.intuit.com/app/developer/qbo/docs/learn/explore-the-quickbooks-online-api/data-queries) |
| [List Customers](actions/list-customers.md) | `GET /query` | [docs](https://developer.intuit.com/app/developer/qbo/docs/learn/explore-the-quickbooks-online-api/data-queries) |
| [List Invoices](actions/list-invoices.md) | `GET /query` | [docs](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/most-commonly-used/invoice#query-an-invoice) |
| [List Items](actions/list-items.md) | `GET /query` | [docs](https://developer.intuit.com/app/developer/qbo/docs/learn/explore-the-quickbooks-online-api/data-queries) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `GET /query` | [docs](https://developer.intuit.com/app/developer/qbo/docs/learn/explore-the-quickbooks-online-api/data-queries) |
| [List Sales Receipts](actions/list-sales-receipts.md) | `GET /query` | [docs](https://developer.intuit.com/app/developer/qbo/docs/learn/explore-the-quickbooks-online-api/data-queries) |
| [List Vendors](actions/list-vendors.md) | `GET /query` | [docs](https://developer.intuit.com/app/developer/qbo/docs/learn/explore-the-quickbooks-online-api/data-queries) |
| [Query](actions/query.md) | `GET /query` | [docs](https://developer.intuit.com/app/developer/qbo/docs/learn/explore-the-quickbooks-online-api/data-queries) |
| [Send Invoice](actions/send-invoice.md) | `POST /invoice/:invoiceId/send` | [docs](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/invoice#send-an-invoice) |
| [Update Customer](actions/update-customer.md) | `POST /customer` | [docs](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/customer#full-update-a-customer) |
| [Update Invoice](actions/update-invoice.md) | `POST /invoice` | [docs](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/invoice#create-an-invoice) |
| [Update Sales Receipt](actions/update-sales-receipt.md) | `POST /salesreceipt` | [docs](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/purchaseorder#create-a-purchaseorder) |
