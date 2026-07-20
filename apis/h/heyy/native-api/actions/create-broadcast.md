# Create Broadcast with Heyy

Creates a new broadcast in a Heyy channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/[:channelId]/broadcasts`
- **Base URL:** `https://api.heyy.io/api/v2.0/`
- **Official documentation:** [Create Broadcast](https://docs.heyy.io/api-reference/create-broadcast)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | The Heyy channel ID. |
| `contacts[]` | body | `array<object>` | no | The contacts payload. |
| `isReoccurring` | body | `boolean` | no | Whether the broadcast repeats. |
| `isScheduled` | body | `boolean` | no | Whether the broadcast is scheduled. |
| `messageTemplateId` | body | `string` | no | The message template ID. |
| `name` | body | `string` | yes | The broadcast name. |
| `recurrenceRules[]` | body | `array<string>` | no | The recurrence rules array. |
| `scheduledAt` | body | `string` | no | When the broadcast should run. |
| `variables[]` | body | `array<object>` | no | The broadcast variables. |
| `workflowId` | body | `string` | yes | The workflow ID used by the broadcast. |
