# List Event Types with Calendly

Retrieves event types from Calendly.

## Endpoint

- **Method:** `GET`
- **Path:** `/event_types`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [List Event Types](https://developer.calendly.com/how-to-get-scheduling-page-links-for-team-members-across-the-organization)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | query | `list` | yes | Organization URI filter. Accepted values: `https://api.calendly.com/organizations/e684df12-9454-43ef-8fc4-2d0faa4ec21e`. |
| `user` | query | `list` | no | User URI filter. Accepted values: `https://api.calendly.com/users/264e5a40-147f-45f9-a96c-a6f2f0a91dff`. |
| `active` | query | `boolean` | no | Filter active event types. |
| `sort` | query | `list` | no | Sort order for event types. Accepted values: `name:asc`, `name:desc`. |
