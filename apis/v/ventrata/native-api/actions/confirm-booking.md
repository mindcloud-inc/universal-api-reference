# Confirm Booking with Ventrata

Confirms an existing booking in Ventrata.

## Endpoint

- **Method:** `POST`
- **Path:** `octo/bookings/:uuid/confirm`
- **Base URL:** `https://api.ventrata.com`
- **Official documentation:** [Confirm Booking](https://docs.ventrata.com/octo-core/bookings#post-bookings-uuid-confirm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Booking UUID from Ventrata. |
