# List User Bookings with Flexopus

Retrieves bookings for a specific Flexopus user.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:user_id/bookings`
- **Base URL:** `{tenantBaseUrl}/api/v1`
- **Official documentation:** [List User Bookings](https://flexopus.com/api/docs/#endpoints-GETapi-v1-users--user_id--bookings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | The ID of the user. |
| `from` | query | `date` | yes | The start of the booking window as an ISO timestamp. |
| `to` | query | `date` | yes | The end of the booking window as an ISO timestamp. |
