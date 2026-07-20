# Get Payment Authorization Status with ConnectPay

Retrieves a payment authorization status from ConnectPay.

## Endpoint

- **Method:** `GET`
- **Path:** `/ob/payments/:paymentOrderNo/authorisations/:PaymentAuthId`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Get Payment Authorization Status](https://docs.connectpay.com/docs/#tag/BaaS-Standard-payments/operation/GetAuthorizationStatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PaymentAuthId` | path | `string` | no | Unique payment authentication ID. |
| `paymentOrderNo` | path | `string` | no | Unique payment order number. |
