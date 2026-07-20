# Verify a Paystack transaction with Maildrip

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/payment/paystack/transactions/verify`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Verify a Paystack transaction](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `txref` | query | `string` | yes | The transaction reference. |
| `savecard` | query | `string` | no | Flag indicating whether to save the card or not. |
