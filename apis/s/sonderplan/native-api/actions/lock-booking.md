# Lock Booking with Sonderplan

## Endpoint

- **Method:** `PUT`
- **Path:** `/booking/lock`
- **Base URL:** `https://api.sonderplan.com/v2`
- **Official documentation:** [Lock Booking](https://docs.sonderplan.com/api-reference/booking/lock-booking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Booking lock request payload. |
| `id` | query | `string` | yes | Booking ID to lock. |
