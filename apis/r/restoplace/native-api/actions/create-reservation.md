# Create Reservation with Restoplace

Creates a new reservation in Restoplace.

## Endpoint

- **Method:** `POST`
- **Path:** `/reserves/`
- **Base URL:** `https://api.restoplace.cc`
- **Official documentation:** [Create Reservation](https://restoplace.cc/help/API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | no | Reservation start date and time in the provider-supported format. |
| `to` | body | `string` | no | Reservation end date and time in the provider-supported format. |
| `name` | body | `string` | no | Guest name for the reservation. |
| `phone` | body | `string` | no | Guest phone number. |
| `count` | body | `number` | no | Number of guests for the reservation. |
| `item_ids[]` | body | `array<number>` | no | Booking item IDs to reserve. |
| `text` | body | `string` | no | Optional reservation comment. |
| `email` | body | `string` | no | Guest email address. |
| `tg_username` | body | `string` | no | Telegram username without the @ symbol. |
| `source` | body | `string` | no | Reservation source label such as widget, admin, or api. |
| `floorid` | body | `number` | no | Hall ID to use when the reservation is tied to a hall instead of specific booking items. |
| `tags[]` | body | `array<string>` | no | Reservation tags to attach to the booking. |
| `waitlist` | body | `number` | no | Whether the reservation should be added to the waitlist. |
| `deposit` | body | `number` | no | Whether a deposit should be required for this reservation. |
| `deposit_total` | body | `number` | no | Total deposit amount expected for the reservation. |
| `deposit_paid` | body | `number` | no | Deposit amount already paid for the reservation. |
