# Cancel Booking with Edoobox

Cancels an existing booking in Edoobox.

## Endpoint

- **Method:** `PUT`
- **Path:** `/booking/:booking_id/cancel`
- **Base URL:** `https://app2.edoobox.com/v2`
- **Official documentation:** [Cancel Booking](https://api.docs.edoobox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `booking_id` | path | `string` | yes | edoobox booking ID. |
| `offer` | body | `string` | yes | edoobox offer ID associated with the booking. |
