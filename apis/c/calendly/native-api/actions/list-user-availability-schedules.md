# List User Availability Schedules with Calendly

Retrieves user availability schedules from Calendly.

## Endpoint

- **Method:** `GET`
- **Path:** `/user_availability_schedules`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [List User Availability Schedules](https://developer.calendly.com/view-event-type-and-user-calendar-availability-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | query | `list` | yes | User URI filter. Accepted values: `https://api.calendly.com/users/264e5a40-147f-45f9-a96c-a6f2f0a91dff`. |
