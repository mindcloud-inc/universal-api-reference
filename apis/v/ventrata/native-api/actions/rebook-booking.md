# Rebook Booking with Ventrata

Rebooks an existing booking in Ventrata.

## Endpoint

- **Method:** `POST`
- **Path:** `octo/bookings/:uuid/rebook`
- **Base URL:** `https://api.ventrata.com`
- **Official documentation:** [Rebook Booking](https://docs.ventrata.com/octo-core/bookings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Booking UUID from Ventrata. |
