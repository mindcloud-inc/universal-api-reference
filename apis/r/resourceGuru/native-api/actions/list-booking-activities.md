# List Booking Activities with Resource Guru

Retrieves activities for a booking from Resource Guru.

## Endpoint

- **Method:** `GET`
- **Path:** `/bookings/:id/activities`
- **Base URL:** `https://api.resourceguruapp.com/v1/{accountId}`
- **Official documentation:** [List Booking Activities](https://resourceguruapp.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Booking ID. |
