# List Project Bookings with Resource Guru

Retrieves bookings for a project from Resource Guru.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:id/bookings`
- **Base URL:** `https://api.resourceguruapp.com/v1/{accountId}`
- **Official documentation:** [List Project Bookings](https://resourceguruapp.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Project ID. |
