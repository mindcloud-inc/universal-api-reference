# Authorize Currency Exchange Payment with ConnectPay

Authorizes a currency exchange payment in ConnectPay.

## Endpoint

- **Method:** `POST`
- **Path:** `/ob/currencyexchangepayments/:paymentOrderNo/authorisations/nosca`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Authorize Currency Exchange Payment](https://docs.connectpay.com/docs/#tag/BaaS-FX-payments/operation/AuthorizeCurrencyExchangePayment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paymentOrderNo` | path | `string` | no | Unique payment order number. |
