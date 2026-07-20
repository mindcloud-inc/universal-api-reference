# Update Broadcast with Heyy

Updates an existing broadcast in a Heyy channel.

## Endpoint

- **Method:** `PUT`
- **Path:** `/[:channelId]/broadcasts/:broadcastId`
- **Base URL:** `https://api.heyy.io/api/v2.0/`
- **Official documentation:** [Update Broadcast](https://docs.heyy.io/api-reference/update-broadcast)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcastId` | path | `string` | yes | The Heyy broadcast ID. |
| `channelId` | path | `string` | yes | The Heyy channel ID. |
| `isReoccurring` | body | `boolean` | no | Whether the broadcast is recurring. |
| `isScheduled` | body | `boolean` | no | Whether the broadcast is scheduled. |
| `name` | body | `string` | no | Broadcast name. |
| `recurrenceRules[]` | body | `array<string>` | no | Optional recurrence rules. |
| `scheduledAt` | body | `string` | no | Scheduled send time in ISO 8601 format. |
| `workflowId` | body | `string` | no | The Heyy workflow ID. |
