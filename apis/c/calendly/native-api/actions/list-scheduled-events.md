# List Scheduled Events with Calendly

Retrieves scheduled events from Calendly.

## Endpoint

- **Method:** `GET`
- **Path:** `/scheduled_events`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [List Scheduled Events](https://developer.calendly.com/update-your-system-with-data-from-scheduled-events-admins-only)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | query | `list` | yes | Organization URI filter. Accepted values: `https://api.calendly.com/organizations/e684df12-9454-43ef-8fc4-2d0faa4ec21e`. |
| `user` | query | `list` | no | User URI filter. Accepted values: `https://api.calendly.com/users/264e5a40-147f-45f9-a96c-a6f2f0a91dff`. |
| `min_start_time` | query | `date` | no | Minimum event start timestamp (ISO-8601). |
| `max_start_time` | query | `date` | no | Maximum event start timestamp (ISO-8601). |
| `invitee_email` | query | `string` | no | Filter scheduled events by invitee email. |
| `status` | query | `list` | no | Event status filter. Accepted values: `active`, `canceled`. |
| `group` | query | `string` | no | Group URI filter. |
| `sort` | query | `list` | no | Sort order for scheduled events. Accepted values: `start_time:asc`, `start_time:desc`. |
