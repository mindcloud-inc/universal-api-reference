# Request Booking Reschedule with OnceHub

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/bookings/:id/request-reschedule`
- **Base URL:** `https://api.oncehub.com`
- **Official documentation:** [Request Booking Reschedule](https://developers.oncehub.com/reference/booking-calendars/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The OnceHub booking identifier. |
| `reschedule_reason` | body | `string` | no | Reason to include with the reschedule request. |
