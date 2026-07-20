# List Event Types with Cal.com

Retrieves event types from Cal.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/event-types`
- **Base URL:** `https://api.cal.com/v2`
- **Official documentation:** [List Event Types](https://cal.com/docs/api-reference/v2/event-types/get-all-event-types)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventSlug` | query | `list` | no | Filter event types by event slug. |
| `orgId` | query | `number` | no | Organization ID filter. |
| `orgSlug` | query | `string` | no | Organization slug filter. |
| `sortCreatedAt` | query | `list` | no | Sort direction for creation timestamp (`asc` or `desc`). Accepted values: `asc`, `desc`. |
| `username` | query | `string` | no | Filter event types for a single username. |
| `usernames` | query | `string` | no | Comma-separated usernames for team/event type lookup. |
