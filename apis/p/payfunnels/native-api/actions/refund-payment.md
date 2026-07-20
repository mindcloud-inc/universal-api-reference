# Refund Payment with Payfunnels

Updates a payment by refunding it in Payfunnels.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/payments/refund`
- **Base URL:** `https://api.payfunnels.com`
- **Official documentation:** [Refund Payment](https://api.payfunnels.com/api/docs/#refund-payment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | The amount to refund in the smallest currency unit. |
| `id` | body | `string` | yes | The ID of the payment to refund. |
| `reason` | body | `string` | yes | Reason for the refund: duplicate, fraudulent, or requested_by_customer. |
