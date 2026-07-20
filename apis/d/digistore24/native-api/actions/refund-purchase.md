# Refund Purchase with Digistore24

Refunds all refundable payments for a Digistore24 purchase.

## Endpoint

- **Method:** `POST`
- **Path:** `/refundPurchase`
- **Base URL:** `https://www.digistore24.com/api/call`
- **Official documentation:** [Refund Purchase](https://digistore24.com/api/docs/paths/refundPurchase.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purchase_id` | query | `string` | yes | Purchase ID |
| `force` | query | `boolean` | no | Force refund |
| `request_date` | query | `string` | no | Refund request date |
