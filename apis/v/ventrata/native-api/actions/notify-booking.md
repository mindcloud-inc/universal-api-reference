# Notify Booking with Ventrata

Sends notifications for a booking in Ventrata.

## Endpoint

- **Method:** `POST`
- **Path:** `octo/bookings/:uuid/notify`
- **Base URL:** `https://api.ventrata.com`
- **Official documentation:** [Notify Booking](https://docs.ventrata.com/octo-core/bookings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Booking UUID from Ventrata. |
