# List Tickets with SupportBee

Retrieves tickets from SupportBee.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets`
- **Base URL:** `https://{company}.supportbee.com`
- **Official documentation:** [List Tickets](https://supportbee.com/docs/api/reference#tag/Tickets/paths/~1tickets/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `string` | no | If true, retrieves archived tickets only. If false, archived tickets are excluded. If any, archived tickets are included. |
| `spam` | query | `boolean` | no | If true, retrieves tickets marked as spam. |
| `trash` | query | `boolean` | no | If true, retrieves tickets that are trashed. |
| `replies` | query | `boolean` | no | Filter to tickets with replies or without replies. |
| `max_replies` | query | `number` | no | Retrieve tickets with a specific number of replies. Cannot be used with replies=false. |
| `assigned_user` | query | `string` | no | Use me, any, none, or a SupportBee agent ID. |
| `assigned_team` | query | `string` | no | Use mine, none, or a SupportBee team ID. |
| `label` | query | `string` | no | Retrieve only tickets with the specified label name. |
| `since` | query | `date` | no | Retrieve tickets whose last activity is after the provided date, date-time, or timestamp. |
| `until` | query | `date` | no | Retrieve tickets whose last activity is before the provided date, date-time, or timestamp. |
| `sort_by` | query | `string` | no | Sort tickets by last_activity or creation_time. |
| `requester_emails` | query | `string` | no | Comma-separated requester email addresses. |
| `total_only` | query | `boolean` | no | Return only the total number of matching tickets. |
