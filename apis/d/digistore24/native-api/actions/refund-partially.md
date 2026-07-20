# Refund Partially with Digistore24

Partially refunds a payment in Digistore24 while keeping the order status.

## Endpoint

- **Method:** `POST`
- **Path:** `/refundPartially`
- **Base URL:** `https://www.digistore24.com/api/call`
- **Official documentation:** [Refund Partially](https://digistore24.com/api/docs/paths/refundPartially.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purchase_id` | query | `string` | yes | Purchase ID |
| `amount` | query | `number` | yes | Refund amount |
