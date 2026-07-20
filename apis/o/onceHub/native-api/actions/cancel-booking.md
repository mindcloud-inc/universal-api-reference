# Cancel Booking with OnceHub

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/bookings/:id/cancel`
- **Base URL:** `https://api.oncehub.com`
- **Official documentation:** [Cancel Booking](https://developers.oncehub.com/reference/booking-calendars/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The OnceHub booking identifier. |
| `cancellation_reason` | body | `string` | no | Reason to include with the booking cancellation. |
| `send_cancellation_email` | body | `boolean` | no | Whether OnceHub should email the customer about the cancellation. |
