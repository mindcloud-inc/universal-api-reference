# Get Payment Status with ConnectPay

Retrieves a payment status from ConnectPay.

## Endpoint

- **Method:** `GET`
- **Path:** `/ob/payments/:paymentOrderNo/status`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Get Payment Status](https://docs.connectpay.com/docs/#tag/BaaS-Standard-payments/operation/GetPaymentStatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paymentOrderNo` | path | `string` | no | Unique payment order number. |
