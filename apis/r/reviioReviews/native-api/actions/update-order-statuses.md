# Update Order Statuses with Revi.io Reviews

Updates order statuses in Revi.io Reviews.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders_status`
- **Base URL:** `https://api.revi.io/api/v1`
- **Official documentation:** [Update Order Statuses](https://docs.revi7.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orders[]` | body | `array<object>` | yes | Array of order status objects containing id_order, status, and date_status_upd. |
