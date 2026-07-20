# ConnectPay: Native API Reference

A consolidated summary of ConnectPay's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.connectpay.com/docs/
- **API base URL:** `https://api-stage.connectpay.com`

## Authentication

### OAuth access token

ConnectPay API requests use an OAuth Bearer access token generated from the ConnectPay authCode/token flow. Paste a valid access token into the API key field for this connection.

### Credentials

- **Access token:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.connectpay.com/data-api-access/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size (default 100; accepted range 1–3000). Use `pageNo` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Card](actions/activate-card.md) | `POST /baas/ob/cards/:cardId/activate` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Card-creation-and-details/operation/activateCardByCardId) |
| [Authorize Currency Exchange Payment](actions/authorize-currency-exchange-payment.md) | `POST /ob/currencyexchangepayments/:paymentOrderNo/authorisations/nosca` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-FX-payments/operation/AuthorizeCurrencyExchangePayment) |
| [Authorize Payment](actions/authorize-payment.md) | `POST /ob/payments/:paymentOrderNo/authorisations/nosca` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Standard-payments/operation/AuthorizePayment) |
| [Block Account](actions/block-account.md) | `POST /baas/ob/accounts/:accountId/block` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Accounts/operation/blockAccount) |
| [Change Card PIN](actions/change-card-pin.md) | `PATCH /baas/ob/cards/:cardId/pin` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Card-management/operation/changeCardPin) |
| [Close Account](actions/close-account.md) | `POST /baas/ob/accounts/:accountId/close` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Accounts/operation/closeIBANAccount) |
| [Create Card Application](actions/create-card-application.md) | `POST /baas/ob/clients/:baasClientId/cards` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Card-creation-and-details/operation/createCardApplication) |
| [Freeze Card](actions/freeze-card.md) | `POST /baas/ob/cards/:cardId/freeze` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Card-management/operation/freezeCard) |
| [Get Account Transactions](actions/get-account-transactions.md) | `GET /ob/accounts/:accountId/transactions` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Accounts/operation/getAccountTransactions) |
| [Get Accounts](actions/get-accounts.md) | `GET /ob/accounts` | [docs](https://docs.connectpay.com/docs/#tag/Accounts/operation/getAccounts) |
| [Get BaaS Client Account Details](actions/get-baas-client-account-details.md) | `GET /ob/baas/clients/:baasClientId/accounts/:accountId` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Accounts/operation/getAccountDetailsByAccountId) |
| [Get BaaS Client Accounts](actions/get-baas-client-accounts.md) | `GET /ob/baas/clients/:baasClientId/accounts` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Accounts/operation/getBaasClientAccountsByClientId) |
| [Get BaaS Client Cards](actions/get-baas-client-cards.md) | `GET /baas/ob/baas/clients/:baasClientId/cards` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Card-creation-and-details/operation/getBaaSClientCards) |
| [Get BaaS Clients](actions/get-baas-clients.md) | `GET /ob/baas/clients` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Clients/operation/getBaaSClients) |
| [Get BaaS Merchant Payment Details](actions/get-baas-merchant-payment-details.md) | `GET /baas/merchant/payments/:paymentId` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Merchant-payments-and-providers/operation/GetPaymentDetailsById) |
| [Get BaaS Merchant Providers](actions/get-baas-merchant-providers.md) | `GET /baas/merchant/brands/:BaaSClientBrandId/providers` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Merchant-payments-and-providers/operation/GetProviders) |
| [Get BaaS Merchant Recurrence Details](actions/get-baas-merchant-recurrence-details.md) | `GET /baas/merchant/recurrences/:recurrenceId` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Merchant-recurrences/operation/GetRecurrencesDetailsById) |
| [Get Card Authorisation Details](actions/get-card-authorisation-details.md) | `GET /baas/ob/cards/:cardId/authorisation/:authorisationId` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Card-creation-and-details/operation/getCardAuthorisationById) |
| [Get Card Details](actions/get-card-details.md) | `GET /baas/ob/cards/:cardId` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Card-creation-and-details/operation/getCardDetailsByCardId) |
| [Get Card Number](actions/get-card-number.md) | `POST /baas/ob/cards/:cardId/encryptedpan` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Card-creation-and-details/operation/getCardEncryptedPan) |
| [Get Currency Exchange Payment Details](actions/get-currency-exchange-payment-details.md) | `GET /ob/currencyexchangepayments/:paymentOrderNo` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-FX-payments/operation/GetCurrencyExchangePaymentDetails) |
| [Get CVV2](actions/get-cvv2.md) | `POST /baas/ob/cards/:cardId/encryptedcvv2` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Card-creation-and-details/operation/getCardEncryptedCvv2) |
| [Get Encrypted PIN](actions/get-encrypted-pin.md) | `POST /baas/ob/cards/:cardId/encryptedpin` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Card-creation-and-details/operation/getCardEncryptedPin) |
| [Get Exchange Rates](actions/get-exchange-rates.md) | `GET /ob/currencyexchangerate` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-FX-payments/operation/GetFxRates) |
| [Get Payment Authorization Status](actions/get-payment-authorization-status.md) | `GET /ob/payments/:paymentOrderNo/authorisations/:PaymentAuthId` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Standard-payments/operation/GetAuthorizationStatus) |
| [Get Payment Details](actions/get-payment-details.md) | `GET /ob/payments/:paymentOrderNo` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Standard-payments/operation/GetPaymentDetails) |
| [Get Payment Rails](actions/get-payment-rails.md) | `POST /ob/paymentrails` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Standard-payments/operation/GetPaymentRails) |
| [Get Payment Status](actions/get-payment-status.md) | `GET /ob/payments/:paymentOrderNo/status` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Standard-payments/operation/GetPaymentStatus) |
| [Initiate Currency Exchange Payment](actions/initiate-currency-exchange-payment.md) | `POST /ob/currencyexchangepayments` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-FX-payments/operation/InitiateCurrencyExchangePayment) |
| [Initiate Fee Payment](actions/initiate-fee-payment.md) | `POST /ob/feepayments` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Standard-payments/operation/InitiateFeePayment) |
| [Initiate Payment](actions/initiate-payment.md) | `POST /ob/payments` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Standard-payments/operation/InitiatePayment) |
| [Open Account](actions/open-account.md) | `POST /baas/ob/accounts` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Accounts/operation/openIBANAccount) |
| [Recall Payment](actions/recall-payment.md) | `POST /ob/recallpayments` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Standard-payments/operation/RecallPayment) |
| [Terminate Card](actions/terminate-card.md) | `POST /baas/ob/cards/:cardId/close` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Card-management/operation/terminateCard) |
| [Unfreeze Card](actions/unfreeze-card.md) | `POST /baas/ob/cards/:cardId/unfreeze` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Card-management/operation/unfreezeCard) |
| [Update Card Delivery Address](actions/update-card-delivery-address.md) | `PATCH /baas/ob/cards/:cardId/deliveryaddress` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Card-management/operation/updateCardDeliveryAddress) |
| [Update Card Limits](actions/update-card-limits.md) | `PATCH /baas/ob/cards/:cardId/limits` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Card-management/operation/updateCardLimitsByCardId) |
| [Update Card Renewal Settings](actions/update-card-renewal-settings.md) | `PATCH /baas/ob/cards/:cardId/automaticrenewal` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Card-management/operation/updateCardRenewalSettings) |
| [Update Card Security Settings](actions/update-card-security-settings.md) | `PATCH /baas/ob/cards/:cardId/security` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Card-management/operation/updateCardSecurity) |
| [Update Card 3DS Settings](actions/update-card3ds-settings.md) | `PATCH /baas/ob/cards/:cardId/update3ds` | [docs](https://docs.connectpay.com/docs/#tag/BaaS-Card-management/operation/updateCard3DSecureSettings) |
