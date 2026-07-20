# List User Bookings by Email with Flexopus

Retrieves bookings for a Flexopus user by email.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/by-email/:user_email/bookings`
- **Base URL:** `{tenantBaseUrl}/api/v1`
- **Official documentation:** [List User Bookings by Email](https://flexopus.com/api/docs/#endpoints-GETapi-v1-users-by-email--user_email--bookings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_email` | path | `string` | yes | The email address of the user. |
| `from` | query | `date` | yes | The start of the booking window as an ISO timestamp. |
| `to` | query | `date` | yes | The end of the booking window as an ISO timestamp. |
