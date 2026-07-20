# Remind Booking with Resource Guru

Sends a booking reminder in Resource Guru.

## Endpoint

- **Method:** `POST`
- **Path:** `/bookings/:id/remind`
- **Base URL:** `https://api.resourceguruapp.com/v1/{accountId}`
- **Official documentation:** [Remind Booking](https://resourceguruapp.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Booking ID. |
