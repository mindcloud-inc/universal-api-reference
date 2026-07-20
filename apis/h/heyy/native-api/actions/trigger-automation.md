# Trigger Automation with Heyy

Triggers an automation in a Heyy channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/[:channelId]/workflows/:workflowId`
- **Base URL:** `https://api.heyy.io/api/v2.0/`
- **Official documentation:** [Trigger Automation](https://docs.heyy.io/api-reference/trigger-automation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | The Heyy channel ID. |
| `phoneNumber` | body | `string` | yes | The destination phone number. |
| `scheduledAt` | body | `string` | no | Optional scheduled send time in ISO 8601 format. |
| `variables[]` | body | `array<object>` | no | Optional template variables. |
| `workflowId` | path | `string` | yes | The Heyy workflow ID. |
