# Cancel Booking with Ventrata

Cancels an existing booking in Ventrata.

## Endpoint

- **Method:** `POST`
- **Path:** `octo/bookings/:uuid/cancel`
- **Base URL:** `https://api.ventrata.com`
- **Official documentation:** [Cancel Booking](https://docs.ventrata.com/octo-core/bookings#post-bookings-uuid-cancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Booking UUID from Ventrata. |
