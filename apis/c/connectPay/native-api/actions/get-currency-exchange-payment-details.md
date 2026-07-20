# Get Currency Exchange Payment Details with ConnectPay

Retrieves currency exchange payment details from ConnectPay.

## Endpoint

- **Method:** `GET`
- **Path:** `/ob/currencyexchangepayments/:paymentOrderNo`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Get Currency Exchange Payment Details](https://docs.connectpay.com/docs/#tag/BaaS-FX-payments/operation/GetCurrencyExchangePaymentDetails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paymentOrderNo` | path | `string` | no | Unique payment order number. |
