# Detokenize Payment Method with Global Payments WebPay

Retrieves detokenized payment method details from Global Payments WebPay.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment-methods/{id}/detokenize`
- **Base URL:** `https://apis.globalpay.com/ucp`
- **Official documentation:** [Detokenize Payment Method](https://developer.globalpayments.com/api/payment-methods-tokenization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Global Payments payment method ID. |
