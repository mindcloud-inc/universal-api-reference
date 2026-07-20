# List Client Bookings with Resource Guru

Retrieves bookings for a client from Resource Guru.

## Endpoint

- **Method:** `GET`
- **Path:** `/clients/:id/bookings`
- **Base URL:** `https://api.resourceguruapp.com/v1/{accountId}`
- **Official documentation:** [List Client Bookings](https://resourceguruapp.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Client ID. |
