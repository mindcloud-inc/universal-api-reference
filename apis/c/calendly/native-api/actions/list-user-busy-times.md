# List User Busy Times with Calendly

Retrieves user busy times from Calendly.

## Endpoint

- **Method:** `GET`
- **Path:** `/user_busy_times`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [List User Busy Times](https://developer.calendly.com/view-event-type-and-user-calendar-availability-data)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | query | `list` | yes | User URI filter. Accepted values: `https://api.calendly.com/users/264e5a40-147f-45f9-a96c-a6f2f0a91dff`. |
| `start_time` | query | `date` | yes | Start of interval (ISO-8601). |
| `end_time` | query | `date` | yes | End of interval (ISO-8601). |
