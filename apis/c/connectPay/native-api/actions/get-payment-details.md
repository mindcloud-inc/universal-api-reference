# Get Payment Details with ConnectPay

Retrieves payment details from ConnectPay.

## Endpoint

- **Method:** `GET`
- **Path:** `/ob/payments/:paymentOrderNo`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Get Payment Details](https://docs.connectpay.com/docs/#tag/BaaS-Standard-payments/operation/GetPaymentDetails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paymentOrderNo` | path | `string` | no | Unique payment order number. |
