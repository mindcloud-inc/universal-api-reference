# List Resource Bookings with Resource Guru

Retrieves bookings for a resource from Resource Guru.

## Endpoint

- **Method:** `GET`
- **Path:** `/resources/:id/bookings`
- **Base URL:** `https://api.resourceguruapp.com/v1/{accountId}`
- **Official documentation:** [List Resource Bookings](https://resourceguruapp.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Resource ID. |
