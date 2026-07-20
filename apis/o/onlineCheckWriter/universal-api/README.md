# <img src="https://images.mindcloud.co/apps/icons/images-1_1774980115233.png" alt="OnlineCheckWriter logo" width="28" height="28"> OnlineCheckWriter: Universal API

Send payments, print checks, and manage wallets and payees

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/onlineCheckWriter/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.onlinecheckwriter.com
- **Vendor API docs:** https://apiv3.onlinecheckwriter.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Wallets](actions/list-wallets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/list-wallets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Bank Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Bank Accounts](actions/create-bank-accounts.md) | POST | Creates up to 20 bank accounts in a single request. |
| [Delete Bank Account](actions/delete-bank-account.md) | DELETE | Deletes an existing bank account. |
| [Get Bank Account](actions/get-bank-account.md) | GET | Retrieves details for a specific bank account. |
| [List Bank Accounts](actions/list-bank-accounts.md) | GET | Lists bank accounts in the connected OnlineCheckWriter account. |
| [Update Bank Account](actions/update-bank-account.md) | PUT | Updates an existing bank account. |
| [Validate Routing Number](actions/validate-routing-number.md) | GET | Validates a bank routing number. |

### Bank Account Template

| Action | Method | Description |
| --- | --- | --- |
| [List Bank Account Templates](actions/list-bank-account-templates.md) | GET | Lists available check design templates for bank accounts. |

### Check

| Action | Method | Description |
| --- | --- | --- |
| [Create Check](actions/create-check.md) | POST | Creates one or more checks in a single request. |
| [Delete Check](actions/delete-check.md) | DELETE | Deletes an existing check. |
| [Get Check](actions/get-check.md) | GET | Retrieves details for a specific check. |
| [List Checks](actions/list-checks.md) | GET | Lists checks in the connected OnlineCheckWriter account. |
| [Mark Check as Cleared](actions/mark-check-as-cleared.md) | PUT | Marks a specific check as cleared. |
| [Print Checks](actions/print-checks.md) | POST | Prints one or more checks using the selected paper type. |
| [Update Check](actions/update-check.md) | PUT | Updates an existing check. |
| [Void Check](actions/void-check.md) | PUT | Voids a specific check. |

### Mail Check

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Mail Check Fee](actions/calculate-mail-check-fee.md) | GET | Calculates fees for a mail check request. |
| [Create Mail Check](actions/create-mail-check.md) | POST | Creates one or more mail checks. |
| [Track Mail Check](actions/track-mail-check.md) | GET | Retrieves tracking details for a mailed check. |

### Mail Check Mailing Option

| Action | Method | Description |
| --- | --- | --- |
| [List Mail Check Mailing Options](actions/list-mail-check-mailing-options.md) | GET | Lists available mailing, paper, and insert options for mail checks. |

### Payee

| Action | Method | Description |
| --- | --- | --- |
| [Create Payee](actions/create-payee.md) | POST | Creates one or more payees in a single request. |
| [Delete Payee](actions/delete-payee.md) | DELETE | Deletes an existing payee. |
| [Get Payee](actions/get-payee.md) | GET | Retrieves details for a specific payee. |
| [List Payees](actions/list-payees.md) | GET | Lists payees in the connected OnlineCheckWriter account. |
| [Update Payee](actions/update-payee.md) | PUT | Updates an existing payee. |

### Payee Bank Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Payee Bank Account](actions/create-payee-bank-account.md) | POST | Creates a bank account for a specific payee. |
| [Get Payee Bank Account](actions/get-payee-bank-account.md) | GET | Retrieves a specific bank account for a payee. |
| [List Payee Bank Accounts](actions/list-payee-bank-accounts.md) | GET | Lists bank accounts for a specific payee. |
| [Update Payee Bank Account](actions/update-payee-bank-account.md) | PUT | Updates a specific bank account for a payee. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Get Payment Info](actions/get-payment-info.md) | GET | Retrieves the status and details of a specific payment. |
| [Send ACH Payment](actions/send-ach-payment.md) | POST | Initiates an ACH payment from a wallet or bank account. |
| [Send Check Mail Payment](actions/send-check-mail-payment.md) | POST | Initiates a check mail payment from a wallet. |
| [Send Wire Payment](actions/send-wire-payment.md) | POST | Initiates a wire payment from a wallet or bank account. |

### Wallet

| Action | Method | Description |
| --- | --- | --- |
| [Get Wallet](actions/get-wallet.md) | GET | Retrieves details for a specific wallet. |
| [List Wallets](actions/list-wallets.md) | GET | Lists wallets available in the connected OnlineCheckWriter account. |

### Wallet Funding

| Action | Method | Description |
| --- | --- | --- |
| [Get ACH Wallet Funding](actions/get-ach-wallet-funding.md) | GET | Retrieves the status and details of a specific ACH wallet funding request. |
| [Initiate ACH Wallet Funding](actions/initiate-ach-wallet-funding.md) | POST | Initiates ACH funding for a wallet. |
| [List ACH Wallet Funding](actions/list-ach-wallet-funding.md) | GET | Lists ACH wallet funding requests. |

### Wallet Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Wallet Transactions](actions/list-wallet-transactions.md) | GET | Lists transactions for a specific wallet. |

### Wallet Withdrawal

| Action | Method | Description |
| --- | --- | --- |
| [Get ACH Withdrawal](actions/get-ach-withdrawal.md) | GET | Retrieves the status and details of a specific ACH withdrawal. |
| [Initiate ACH Withdrawal](actions/initiate-ach-withdrawal.md) | POST | Initiates an ACH withdrawal from a wallet. |

