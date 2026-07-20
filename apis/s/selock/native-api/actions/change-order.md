# Change Order with Selock

## Endpoint

- **Method:** `POST`
- **Path:** `/zaiper/change_order/`
- **Base URL:** `https://selock.co/api/v1`
- **Official documentation:** [Change Order](https://selock.co/en/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | body | `number` | yes | Selock order identifier. |
| `start_date` | body | `string` | no | Check-in date in DD-MM-YYYY format. |
| `hour_in` | body | `number` | no | Check-in hour as an integer. |
| `end_date` | body | `string` | no | Check-out date in DD-MM-YYYY format. |
| `hour_out` | body | `number` | no | Check-out hour as an integer. |
| `room_id` | body | `number` | no | Target room identifier when available. |
| `room_name` | body | `string` | no | Target room name when using name-based lookup. |
| `comment` | body | `string` | no | Order comment. |
| `price` | body | `number` | no | Order price. |
| `paid` | body | `number` | no | Amount already paid. |
| `confirmed` | body | `boolean` | no | Whether the order is confirmed. |
| `busy` | body | `boolean` | no | Whether the order is busy/checked in. |
| `canceled` | body | `boolean` | no | Whether the order is canceled. |
| `language` | body | `string` | no | Language name from the Selock account. |
| `source` | body | `string` | no | Source name from the Selock account. |
