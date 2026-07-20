# List Conversations with SuperSend

Retrieves conversations from SuperSend.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [List Conversations](https://docs.supersend.io/docs/conversation)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | query | `string` | no | Filter by team ID (UUID from list teams) |
| `channel` | query | `string` | no | Allowed values: email, linkedin, twitter. Default: linkedin. |
| `last_message_direction` | query | `string` | no | Allowed values: inbound, outbound. |
| `identity_id` | query | `string` | no | — |
| `status` | query | `string` | no | Allowed values: archived, unarchived. |
| `read_status` | query | `string` | no | Allowed values: read, unread. |
| `search` | query | `string` | no | — |
| `sort_by` | query | `string` | no | Sort field (default date) Allowed values: date. |
| `sort_direction` | query | `string` | no | Allowed values: asc, desc. Default: desc. |
| `limit` | query | `number` | no | Default: 50. Range: 1 to 100. |
| `offset` | query | `number` | no | Default: 0. Range: 0 to inf. |
