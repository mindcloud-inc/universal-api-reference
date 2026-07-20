# Refund Transaction with Digistore24

Refunds a payment transaction in Digistore24.

## Endpoint

- **Method:** `POST`
- **Path:** `/refundTransaction`
- **Base URL:** `https://www.digistore24.com/api/call`
- **Official documentation:** [Refund Transaction](https://digistore24.com/api/docs/paths/refundTransaction.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction_id` | query | `string` | yes | Transaction ID |
| `force` | query | `boolean` | no | Force refund |
| `request_date` | query | `string` | no | Refund request date |
