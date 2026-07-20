# QuickFile: Native API Reference

A consolidated summary of QuickFile's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://api.quickfile.co.uk/
- **API base URL:** `https://api.quickfile.co.uk/1_2`

## Authentication

### QuickFile Signed Request

Custom signed-request authentication for the QuickFile API using account number, API key, application ID, a unique submission number, and an MD5 signature.

### Credentials

- **Account Number:** `accountNumber` · required · The QuickFile account number used to authenticate API requests.
- **Application ID:** `applicationId` · required · The QuickFile Application ID for this registered integration.
- **API Key:** `apiKey` · required · The static QuickFile API key from account settings.

[Official authentication documentation](https://api.quickfile.co.uk/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | `POST /client/create` | [docs](https://api.quickfile.co.uk/d/v1_2/Client_Create) |
| [Create Note](actions/create-note.md) | `POST /system/createnote` | [docs](https://api.quickfile.co.uk/d/v1_2/System_CreateNote) |
| [Create Payment](actions/create-payment.md) | `POST /payment/create` | [docs](https://api.quickfile.co.uk/d/v1_2/Payment_Create) |
| [Create Supplier](actions/create-supplier.md) | `POST /supplier/create` | [docs](https://api.quickfile.co.uk/d/v1_2/Supplier_Create) |
| [Get Account Details](actions/get-account-details.md) | `POST /system/getaccountdetails` | [docs](https://api.quickfile.co.uk/d/v1_2/System_GetAccountDetails) |
| [Get Balance Sheet](actions/get-balance-sheet.md) | `POST /report/balancesheet` | [docs](https://api.quickfile.co.uk/d/v1_2/Report_BalanceSheet) |
| [Get Chart Of Accounts](actions/get-chart-of-accounts.md) | `POST /report/chartofaccounts` | [docs](https://api.quickfile.co.uk/d/v1_2/Report_ChartOfAccounts) |
| [Get Client](actions/get-client.md) | `POST /client/get` | [docs](https://api.quickfile.co.uk/d/v1_2/Client_Get) |
| [Get Invoice](actions/get-invoice.md) | `POST /invoice/get` | [docs](https://api.quickfile.co.uk/d/v1_2/Invoice_Get) |
| [Get Invoice PDF](actions/get-invoice-pdf.md) | `POST /invoice/getpdf` | [docs](https://api.quickfile.co.uk/d/v1_2/Invoice_GetPDF) |
| [Get Journal](actions/get-journal.md) | `POST /journal/get` | [docs](https://api.quickfile.co.uk/d/v1_2/Journal_Get) |
| [Get Payment](actions/get-payment.md) | `POST /payment/get` | [docs](https://api.quickfile.co.uk/d/v1_2/Payment_Get) |
| [Get Profit And Loss](actions/get-profit-and-loss.md) | `POST /report/profitandloss` | [docs](https://api.quickfile.co.uk/d/v1_2/Report_ProfitAndLoss) |
| [Get Purchase](actions/get-purchase.md) | `POST /purchase/get` | [docs](https://api.quickfile.co.uk/d/v1_2/Purchase_Get) |
| [Get Supplier](actions/get-supplier.md) | `POST /supplier/get` | [docs](https://api.quickfile.co.uk/d/v1_2/Supplier_Get) |
| [List Bank Account Balances](actions/list-bank-account-balances.md) | `POST /bank/getaccountbalances` | [docs](https://api.quickfile.co.uk/d/v1_2/Bank_GetAccountBalances) |
| [List Bank Accounts](actions/list-bank-accounts.md) | `POST /bank/getaccounts` | [docs](https://api.quickfile.co.uk/d/v1_2/Bank_GetAccounts) |
| [List Payment Methods](actions/list-payment-methods.md) | `POST /payment/getpaymethods` | [docs](https://api.quickfile.co.uk/d/v1_2/Payment_GetPayMethods) |
| [Search Bank Transactions](actions/search-bank-transactions.md) | `POST /bank/search` | [docs](https://api.quickfile.co.uk/d/v1_2/Bank_Search) |
| [Search Clients](actions/search-clients.md) | `POST /client/search` | [docs](https://api.quickfile.co.uk/d/v1_2/Client_Search) |
| [Search Events](actions/search-events.md) | `POST /system/searchevents` | [docs](https://api.quickfile.co.uk/d/v1_2/System_SearchEvents) |
| [Search Invoices](actions/search-invoices.md) | `POST /invoice/search` | [docs](https://api.quickfile.co.uk/d/v1_2/Invoice_Search) |
| [Search Journals](actions/search-journals.md) | `POST /journal/search` | [docs](https://api.quickfile.co.uk/d/v1_2/Journal_Search) |
| [Search Payments](actions/search-payments.md) | `POST /payment/search` | [docs](https://api.quickfile.co.uk/d/v1_2/Payment_Search) |
| [Search Purchases](actions/search-purchases.md) | `POST /purchase/search` | [docs](https://api.quickfile.co.uk/d/v1_2/Purchase_Search) |
| [Search Suppliers](actions/search-suppliers.md) | `POST /supplier/search` | [docs](https://api.quickfile.co.uk/d/v1_2/Supplier_Search) |
| [Update Client](actions/update-client.md) | `POST /client/update` | [docs](https://api.quickfile.co.uk/d/v1_2/Client_Update) |
| [Update Supplier](actions/update-supplier.md) | `POST /supplier/update` | [docs](https://api.quickfile.co.uk/d/v1_2/Supplier_Update) |
