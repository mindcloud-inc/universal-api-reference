# <img src="https://images.mindcloud.co/apps/icons/truelayer-square-icon_1776801414082.png" alt="TrueLayer logo" width="28" height="28"> TrueLayer: Universal API

TrueLayer API integration for sandbox payments, merchant accounts, mandates, payment links, payment providers, Data API account/card access, and verification.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/trueLayer/latest
- **Actions:** 63
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://truelayer.com
- **Vendor API docs:** https://docs.truelayer.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Merchant Accounts](actions/list-merchant-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/list-merchant-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (63)

### Account Details Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify France Account Details](actions/verify-france-account-details.md) | POST | Verifies French account details in TrueLayer. |

### Account Holder Verification

| Action | Method | Description |
| --- | --- | --- |
| [Create Account Holder Verification](actions/create-account-holder-verification.md) | POST | Creates an account holder verification in TrueLayer. |
| [Get Account Holder Verification](actions/get-account-holder-verification.md) | GET | Retrieves an account holder verification from TrueLayer. |
| [Verify Account Holder Name](actions/verify-account-holder-name.md) | POST | Verifies an account holder name in TrueLayer. |

### Bank Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Bank Lookup](actions/bank-lookup.md) | GET | Looks up bank details in TrueLayer. |

### Data Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Account](actions/get-data-account.md) | GET | Retrieves a data account from TrueLayer. |
| [List Data Accounts](actions/list-data-accounts.md) | GET | Retrieves data accounts from TrueLayer. |

### Data Account Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Account Balance](actions/get-data-account-balance.md) | GET | Retrieves a data account balance from TrueLayer. |

### Data Account Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Account Transactions](actions/get-data-account-transactions.md) | GET | Retrieves data account transactions from TrueLayer. |

### Data Card

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Card](actions/get-data-card.md) | GET | Retrieves a data card from TrueLayer. |
| [List Data Cards](actions/list-data-cards.md) | GET | Retrieves data cards from TrueLayer. |

### Data Card Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Card Balance](actions/get-data-card-balance.md) | GET | Retrieves a data card balance from TrueLayer. |

### Data Card Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Card Transactions](actions/get-data-card-transactions.md) | GET | Retrieves data card transactions from TrueLayer. |

### Data Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Info](actions/get-data-info.md) | GET | Retrieves Data API user info from TrueLayer. |

### Data Provider

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Providers](actions/get-data-providers.md) | GET | Retrieves data providers from TrueLayer. |

### Direct Debit

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Account Direct Debits](actions/get-data-account-direct-debits.md) | GET | Retrieves data account direct debits from TrueLayer. |

### Legacy Payment

| Action | Method | Description |
| --- | --- | --- |
| [Legacy Get Payment](actions/legacy-get-payment.md) | GET | Retrieves a legacy payment from TrueLayer. |
| [Legacy Initiate Payment](actions/legacy-initiate-payment.md) | POST | Initiates a legacy payment in TrueLayer. |
| [Legacy Submit Embedded Payment Step](actions/legacy-submit-embedded-payment-step.md) | PUT | Submits a legacy embedded payment step in TrueLayer. |

### Legacy Payment Provider

| Action | Method | Description |
| --- | --- | --- |
| [Legacy List Payment Providers](actions/legacy-list-payment-providers.md) | GET | Retrieves legacy payment providers from TrueLayer. |

### Mandate

| Action | Method | Description |
| --- | --- | --- |
| [Create Mandate](actions/create-mandate.md) | POST | Creates a mandate in TrueLayer. |
| [Get Mandate](actions/get-mandate.md) | GET | Retrieves a mandate from TrueLayer. |
| [List Mandates](actions/list-mandates.md) | GET | Retrieves mandates from TrueLayer. |
| [Revoke Mandate](actions/revoke-mandate.md) | DELETE | Revokes a mandate in TrueLayer. |

### Mandate Authorization Action

| Action | Method | Description |
| --- | --- | --- |
| [Submit Mandate Consent](actions/submit-mandate-consent.md) | POST | Submits mandate consent in TrueLayer. |
| [Submit Mandate Provider Selection](actions/submit-mandate-provider-selection.md) | POST | Submits mandate provider selection in TrueLayer. |

### Mandate Authorization Flow

| Action | Method | Description |
| --- | --- | --- |
| [Start Mandate Authorization Flow](actions/start-mandate-authorization-flow.md) | POST | Starts a mandate authorization flow in TrueLayer. |

### Mandate Constraints

| Action | Method | Description |
| --- | --- | --- |
| [Get Mandate Constraints](actions/get-mandate-constraints.md) | GET | Retrieves mandate constraints from TrueLayer. |

### Mandate Funds

| Action | Method | Description |
| --- | --- | --- |
| [Confirm Mandate Funds](actions/confirm-mandate-funds.md) | GET | Confirms mandate funds in TrueLayer. |

### Merchant Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Merchant Account](actions/get-merchant-account.md) | GET | Retrieves a merchant account from TrueLayer. |
| [List Merchant Accounts](actions/list-merchant-accounts.md) | GET | Retrieves merchant accounts from TrueLayer. |

### Merchant Account Sweeping

| Action | Method | Description |
| --- | --- | --- |
| [Disable Merchant Account Sweeping](actions/disable-merchant-account-sweeping.md) | DELETE | Disables merchant account sweeping in TrueLayer. |
| [Get Merchant Account Sweeping](actions/get-merchant-account-sweeping.md) | GET | Retrieves merchant account sweeping from TrueLayer. |
| [Set Merchant Account Sweeping](actions/set-merchant-account-sweeping.md) | PUT | Sets merchant account sweeping in TrueLayer. |

### Merchant Account Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Merchant Account Transactions](actions/get-merchant-account-transactions.md) | GET | Retrieves merchant account transactions from TrueLayer. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Payment](actions/cancel-payment.md) | PUT | Cancels a payment in TrueLayer. |
| [Create Payment](actions/create-payment.md) | POST | Creates a payment in TrueLayer. |
| [Get Payment](actions/get-payment.md) | GET | Retrieves a payment from TrueLayer. |
| [Get Payment Link Payments](actions/get-payment-link-payments.md) | GET | Retrieves payments for a TrueLayer payment link. |
| [Save Payment User Account](actions/save-payment-user-account.md) | PUT | Saves a payment user account in TrueLayer. |

### Payment Authorization Action

| Action | Method | Description |
| --- | --- | --- |
| [Submit Payment Branch Selection](actions/submit-payment-branch-selection.md) | POST | Submits payment branch selection in TrueLayer. |
| [Submit Payment Consent](actions/submit-payment-consent.md) | POST | Submits payment consent in TrueLayer. |
| [Submit Payment Form](actions/submit-payment-form.md) | POST | Submits a payment authorization form in TrueLayer. |
| [Submit Payment Provider Selection](actions/submit-payment-provider-selection.md) | POST | Submits payment provider selection in TrueLayer. |
| [Submit Payment Scheme Selection](actions/submit-payment-scheme-selection.md) | POST | Submits payment scheme selection in TrueLayer. |
| [Submit Payment User Account Selection](actions/submit-payment-user-account-selection.md) | POST | Submits payment user account selection in TrueLayer. |

### Payment Authorization Flow

| Action | Method | Description |
| --- | --- | --- |
| [Start Payment Authorization Flow](actions/start-payment-authorization-flow.md) | POST | Starts a payment authorization flow in TrueLayer. |

### Payment Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Link](actions/create-payment-link.md) | POST | Creates a payment link in TrueLayer. |
| [Get Payment Link](actions/get-payment-link.md) | GET | Retrieves a payment link from TrueLayer. |

### Payment Provider

| Action | Method | Description |
| --- | --- | --- |
| [Get Payment Provider](actions/get-payment-provider.md) | GET | Retrieves a payment provider from TrueLayer. |
| [Search Payment Providers](actions/search-payment-providers.md) | GET | Searches payment providers in TrueLayer. |

### Payment Refund

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Refund](actions/create-payment-refund.md) | POST | Creates a payment refund in TrueLayer. |
| [Get Payment Refund](actions/get-payment-refund.md) | GET | Retrieves a payment refund from TrueLayer. |
| [Get Payment Refunds](actions/get-payment-refunds.md) | GET | Retrieves payment refunds from TrueLayer. |

### Payment Source

| Action | Method | Description |
| --- | --- | --- |
| [Get Merchant Account Payment Sources](actions/get-merchant-account-payment-sources.md) | GET | Retrieves merchant account payment sources from TrueLayer. |

### Payments Provider Return

| Action | Method | Description |
| --- | --- | --- |
| [Submit Payments Provider Return Parameters](actions/submit-payments-provider-return-parameters.md) | POST | Submits payment provider return parameters in TrueLayer. |

### Payout

| Action | Method | Description |
| --- | --- | --- |
| [Create Payout](actions/create-payout.md) | POST | Creates a payout in TrueLayer. |
| [Get Payout](actions/get-payout.md) | GET | Retrieves a payout from TrueLayer. |

### Payout Authorization Flow

| Action | Method | Description |
| --- | --- | --- |
| [Get Payout Authorization Flow](actions/get-payout-authorization-flow.md) | GET | Retrieves a payout authorization flow from TrueLayer. |
| [Start Payout Authorization Flow](actions/start-payout-authorization-flow.md) | POST | Starts a payout authorization flow in TrueLayer. |

### Signup Plus Account Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Signup Plus Accounts](actions/get-signup-plus-accounts.md) | GET | Retrieves Signup+ accounts from TrueLayer. |

### Signup Plus Mandate Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Signup Plus Mandate Data](actions/get-signup-plus-mandate-data.md) | GET | Retrieves Signup+ mandate data from TrueLayer. |

### Standing Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Account Standing Orders](actions/get-data-account-standing-orders.md) | GET | Retrieves data account standing orders from TrueLayer. |

