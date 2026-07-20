# List Orders with Goldbelly

## Endpoint

- **Method:** `GET`
- **Path:** `orders`
- **Base URL:** `https://api.goldbelly.com/v1/`
- **Official documentation:** [List Orders](https://drive.google.com/file/d/1vH97uUnbEu3v2rs8JrZRi4oNAdp_uqWd/view?usp=sharing#orders_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ship_date` | query | `date` | no | Filters orders to ship on this date. Defaults to today when no date filter is provided. Example: 2019-11-15. |
| `delivery_date` | query | `date` | no | Filters by requested delivery date. Example: 2019-11-15. |
| `order_date` | query | `date` | no | Filters by order completion date. Example: 2019-11-15. |
| `max_days_in_transit` | query | `number` | no | Filters orders by the product's max days in transit. |
| `updated_at_or_after` | query | `date` | no | Filters orders updated at or after this time, or with line items updated at or after this time. Example: 2019-11-15T10:30:00Z. |
