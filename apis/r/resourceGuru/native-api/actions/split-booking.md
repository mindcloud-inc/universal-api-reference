# Split Booking with Resource Guru

Splits a booking in Resource Guru.

## Endpoint

- **Method:** `POST`
- **Path:** `/bookings/:id/split`
- **Base URL:** `https://api.resourceguruapp.com/v1/{accountId}`
- **Official documentation:** [Split Booking](https://resourceguruapp.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Booking ID. |
