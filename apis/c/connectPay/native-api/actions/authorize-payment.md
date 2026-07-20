# Authorize Payment with ConnectPay

Authorizes a payment in ConnectPay.

## Endpoint

- **Method:** `POST`
- **Path:** `/ob/payments/:paymentOrderNo/authorisations/nosca`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Authorize Payment](https://docs.connectpay.com/docs/#tag/BaaS-Standard-payments/operation/AuthorizePayment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paymentOrderNo` | path | `string` | no | Unique payment order number. |
