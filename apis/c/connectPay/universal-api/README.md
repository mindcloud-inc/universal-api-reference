# <img src="https://images.mindcloud.co/apps/icons/favicon-docs-connectpay-com-48x48_1778268785274.png" alt="ConnectPay logo" width="28" height="28"> ConnectPay: Universal API

ConnectPay banking APIs for BaaS clients, accounts, payments, cards, merchant payments, and related payment operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/connectPay/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://connectpay.com
- **Vendor API docs:** https://docs.connectpay.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Transactions](actions/get-account-transactions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/connectPay/latest/actions/get-account-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Bank Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Block Account](actions/block-account.md) | PUT | Blocks an existing account in ConnectPay. |
| [Close Account](actions/close-account.md) | PUT | Closes an existing IBAN account in ConnectPay. |
| [Get Accounts](actions/get-accounts.md) | GET | Retrieves bank accounts from ConnectPay. |
| [Get BaaS Client Account Details](actions/get-baas-client-account-details.md) | GET | Retrieves a BaaS client's account details from ConnectPay. |
| [Get BaaS Client Accounts](actions/get-baas-client-accounts.md) | GET | Retrieves a BaaS client's accounts from ConnectPay. |
| [Open Account](actions/open-account.md) | POST | Opens a new IBAN account in ConnectPay. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get BaaS Clients](actions/get-baas-clients.md) | GET | Retrieves BaaS clients from ConnectPay. |

### Exchange Rates

| Action | Method | Description |
| --- | --- | --- |
| [Get Exchange Rates](actions/get-exchange-rates.md) | GET | Retrieves currency exchange rates from ConnectPay. |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [Activate Card](actions/activate-card.md) | PUT | Activates a ChipAndPin card in ConnectPay. |
| [Change Card PIN](actions/change-card-pin.md) | PUT | Changes a ChipAndPin card PIN in ConnectPay. |
| [Create Card Application](actions/create-card-application.md) | POST | Creates a new card application in ConnectPay. |
| [Freeze Card](actions/freeze-card.md) | PUT | Freezes an existing card in ConnectPay. |
| [Get BaaS Client Cards](actions/get-baas-client-cards.md) | GET | Retrieves a BaaS client's cards from ConnectPay. |
| [Get BaaS Merchant Providers](actions/get-baas-merchant-providers.md) | GET | Retrieves BaaS merchant providers from ConnectPay. |
| [Get Card Details](actions/get-card-details.md) | GET | Retrieves payment card details from ConnectPay. |
| [Terminate Card](actions/terminate-card.md) | PUT | Terminates an existing card in ConnectPay. |
| [Unfreeze Card](actions/unfreeze-card.md) | PUT | Unfreezes an existing card in ConnectPay. |
| [Update Card Delivery Address](actions/update-card-delivery-address.md) | PUT | Updates a ChipAndPin card delivery address in ConnectPay. |
| [Update Card Limits](actions/update-card-limits.md) | PUT | Updates an existing card's limits in ConnectPay. |
| [Update Card Renewal Settings](actions/update-card-renewal-settings.md) | PUT | Enables or disables card renewal in ConnectPay. |
| [Update Card Security Settings](actions/update-card-security-settings.md) | PUT | Updates card security settings in ConnectPay. |
| [Update Card 3DS Settings](actions/update-card3ds-settings.md) | PUT | Updates card 3DS security settings in ConnectPay. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Authorize Currency Exchange Payment](actions/authorize-currency-exchange-payment.md) | PUT | Authorizes a currency exchange payment in ConnectPay. |
| [Authorize Payment](actions/authorize-payment.md) | PUT | Authorizes a payment in ConnectPay. |
| [Get BaaS Merchant Payment Details](actions/get-baas-merchant-payment-details.md) | GET | Retrieves BaaS merchant payment details from ConnectPay. |
| [Get Card Authorisation Details](actions/get-card-authorisation-details.md) | GET | Retrieves card authorisation details from ConnectPay. |
| [Get Currency Exchange Payment Details](actions/get-currency-exchange-payment-details.md) | GET | Retrieves currency exchange payment details from ConnectPay. |
| [Get Payment Authorization Status](actions/get-payment-authorization-status.md) | GET | Retrieves a payment authorization status from ConnectPay. |
| [Get Payment Details](actions/get-payment-details.md) | GET | Retrieves payment details from ConnectPay. |
| [Get Payment Rails](actions/get-payment-rails.md) | GET | Retrieves payment rails from ConnectPay. |
| [Get Payment Status](actions/get-payment-status.md) | GET | Retrieves a payment status from ConnectPay. |
| [Initiate Currency Exchange Payment](actions/initiate-currency-exchange-payment.md) | POST | Initiates a currency exchange payment in ConnectPay. |
| [Initiate Fee Payment](actions/initiate-fee-payment.md) | POST | Initiates a fee payment in ConnectPay. |
| [Initiate Payment](actions/initiate-payment.md) | POST | Initiates a payment in ConnectPay. |
| [Recall Payment](actions/recall-payment.md) | POST | Initiates a payment recall in ConnectPay. |

### Secrets

| Action | Method | Description |
| --- | --- | --- |
| [Get Card Number](actions/get-card-number.md) | GET | Retrieves an encrypted card number from ConnectPay. |
| [Get CVV2](actions/get-cvv2.md) | GET | Retrieves an encrypted card CVV2 from ConnectPay. |
| [Get Encrypted PIN](actions/get-encrypted-pin.md) | GET | Retrieves an encrypted ChipAndPin card PIN from ConnectPay. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Get BaaS Merchant Recurrence Details](actions/get-baas-merchant-recurrence-details.md) | GET | Retrieves BaaS merchant recurrence details from ConnectPay. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Transactions](actions/get-account-transactions.md) | GET | Retrieves bank account transactions from ConnectPay. |

