# Extend Reservation with Ventrata

Extends an existing reservation in Ventrata.

## Endpoint

- **Method:** `POST`
- **Path:** `octo/bookings/:uuid/extend`
- **Base URL:** `https://api.ventrata.com`
- **Official documentation:** [Extend Reservation](https://docs.ventrata.com/octo-core/bookings#post-bookings-uuid-extend)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Booking UUID from Ventrata. |
