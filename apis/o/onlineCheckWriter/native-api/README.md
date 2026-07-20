# OnlineCheckWriter: Native API Reference

A consolidated summary of OnlineCheckWriter's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://apiv3.onlinecheckwriter.com
- **API base URL:** `https://test.onlinecheckwriter.com/api/v3`

## Authentication

### API Key

Use your OnlineCheckWriter API key as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apiv3.onlinecheckwriter.com)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `perPage` in the query string to set the page size (default 10). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Calculate Mail Check Fee](actions/calculate-mail-check-fee.md) | `POST /mailchecks/calculateFee` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Create Bank Accounts](actions/create-bank-accounts.md) | `POST /bankAccounts` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Create Check](actions/create-check.md) | `POST /checks` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Create Mail Check](actions/create-mail-check.md) | `POST /mailchecks` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Create Payee](actions/create-payee.md) | `POST /payees` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Create Payee Bank Account](actions/create-payee-bank-account.md) | `POST /payees/:payeeId/bank-accounts` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Delete Bank Account](actions/delete-bank-account.md) | `DELETE /bankAccounts/:bankAccountId` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Delete Check](actions/delete-check.md) | `DELETE /checks/:checkId` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Delete Payee](actions/delete-payee.md) | `DELETE /payees/:payeeId` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Get ACH Wallet Funding](actions/get-ach-wallet-funding.md) | `GET /wallet/fund-wallet/:walletFundingId` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Get ACH Withdrawal](actions/get-ach-withdrawal.md) | `GET /wallet/withdraw/ach/:withdrawalId` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Get Bank Account](actions/get-bank-account.md) | `GET /bankAccounts/:bankAccountId` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Get Check](actions/get-check.md) | `GET /checks/:checkId` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Get Payee](actions/get-payee.md) | `GET /payees/:payeeId` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Get Payee Bank Account](actions/get-payee-bank-account.md) | `GET /payees/:payeeId/bank-accounts/:payeeBankAccountId` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Get Payment Info](actions/get-payment-info.md) | `GET /send-payment/:paymentId/info` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Get Wallet](actions/get-wallet.md) | `GET /wallet/:walletId` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Initiate ACH Wallet Funding](actions/initiate-ach-wallet-funding.md) | `POST /wallet/fund/ach/initiate` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Initiate ACH Withdrawal](actions/initiate-ach-withdrawal.md) | `POST /wallet/withdraw/ach/initiate` | [docs](https://apiv3.onlinecheckwriter.com) |
| [List ACH Wallet Funding](actions/list-ach-wallet-funding.md) | `GET /wallet/fund/ach` | [docs](https://apiv3.onlinecheckwriter.com) |
| [List Bank Account Templates](actions/list-bank-account-templates.md) | `GET /bankAccounts/templates` | [docs](https://apiv3.onlinecheckwriter.com) |
| [List Bank Accounts](actions/list-bank-accounts.md) | `GET /bankAccounts` | [docs](https://apiv3.onlinecheckwriter.com) |
| [List Checks](actions/list-checks.md) | `GET /checks` | [docs](https://apiv3.onlinecheckwriter.com) |
| [List Mail Check Mailing Options](actions/list-mail-check-mailing-options.md) | `GET /mailchecks/mailingOptions` | [docs](https://apiv3.onlinecheckwriter.com) |
| [List Payee Bank Accounts](actions/list-payee-bank-accounts.md) | `GET /payees/:payeeId/bank-accounts/` | [docs](https://apiv3.onlinecheckwriter.com) |
| [List Payees](actions/list-payees.md) | `GET /payees` | [docs](https://apiv3.onlinecheckwriter.com) |
| [List Wallet Transactions](actions/list-wallet-transactions.md) | `GET /wallet/:walletId/transactions` | [docs](https://apiv3.onlinecheckwriter.com) |
| [List Wallets](actions/list-wallets.md) | `GET /wallet/` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Mark Check as Cleared](actions/mark-check-as-cleared.md) | `POST /checks/:checkId/mark-as-cleared` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Print Checks](actions/print-checks.md) | `POST /checks/print` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Send ACH Payment](actions/send-ach-payment.md) | `POST /send-payment/ach` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Send Check Mail Payment](actions/send-check-mail-payment.md) | `POST /send-payment/checkMail` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Send Wire Payment](actions/send-wire-payment.md) | `POST /send-payment/wire` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Track Mail Check](actions/track-mail-check.md) | `GET /mailchecks/:checkId/tracking` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Update Bank Account](actions/update-bank-account.md) | `PUT /bankAccounts/:bankAccountId` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Update Check](actions/update-check.md) | `PUT /checks/:checkId` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Update Payee](actions/update-payee.md) | `PUT /payees/:payeeId` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Update Payee Bank Account](actions/update-payee-bank-account.md) | `PUT /payees/:payeeId/bank-accounts/:payeeBankAccountId` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Validate Routing Number](actions/validate-routing-number.md) | `POST /bankAccounts/routing-number/:routingNumber` | [docs](https://apiv3.onlinecheckwriter.com) |
| [Void Check](actions/void-check.md) | `POST /checks/:checkId/void` | [docs](https://apiv3.onlinecheckwriter.com) |
