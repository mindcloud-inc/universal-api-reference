# Update Reservation with Restoplace

Updates an existing reservation in Restoplace.

## Endpoint

- **Method:** `PUT`
- **Path:** `/reserves/:id`
- **Base URL:** `https://api.restoplace.cc`
- **Official documentation:** [Update Reservation](https://restoplace.cc/help/API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Unique Restoplace reservation ID. |
| `from` | body | `string` | no | Updated reservation start date and time. |
| `to` | body | `string` | no | Updated reservation end date and time. |
| `name` | body | `string` | no | Updated guest name. |
| `phone` | body | `string` | no | Updated guest phone number. |
| `count` | body | `number` | no | Updated number of guests. |
| `item_ids[]` | body | `array<number>` | no | Updated booking item IDs. |
| `text` | body | `string` | no | Updated reservation comment. |
| `email` | body | `string` | no | Updated guest email address. |
| `tg_username` | body | `string` | no | Updated Telegram username without the @ symbol. |
| `source` | body | `string` | no | Updated reservation source label. |
| `floorid` | body | `number` | no | Updated hall ID. |
| `tags[]` | body | `array<string>` | no | Updated reservation tags. |
| `waitlist` | body | `number` | no | Whether to move the reservation to the waitlist. |
| `deposit` | body | `number` | no | Whether a deposit should be required. |
| `deposit_total` | body | `number` | no | Updated total deposit amount. |
| `deposit_paid` | body | `number` | no | Updated paid deposit amount. |
