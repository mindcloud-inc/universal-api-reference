# Bulk Update Orders with Goldbelly

## Endpoint

- **Method:** `POST`
- **Path:** `orders/bulk_update`
- **Base URL:** `https://api.goldbelly.com/v1/`
- **Official documentation:** [Bulk Update Orders](https://drive.google.com/file/d/1vH97uUnbEu3v2rs8JrZRi4oNAdp_uqWd/view?usp=sharing#orders_bulk_update_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orders[]` | body | `array<object>` | yes | Orders to update. Each item must include a customer reference number and may include merchant status or tracking number. |
| `customer_reference_number` | body | `number` | yes | Customer reference number for the order to update. |
| `merchant_status` | body | `string` | no | Merchant status to set for the order. |
| `tracking_number` | body | `string` | no | Tracking number to set for the order. |
