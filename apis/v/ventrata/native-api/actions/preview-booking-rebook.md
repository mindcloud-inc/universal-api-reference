# Preview Booking Rebook with Ventrata

Previews an existing booking rebook in Ventrata.

## Endpoint

- **Method:** `POST`
- **Path:** `octo/bookings/:uuid/rebook/preview`
- **Base URL:** `https://api.ventrata.com`
- **Official documentation:** [Preview Booking Rebook](https://docs.ventrata.com/octo-core/bookings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Booking UUID from Ventrata. |
