# Snooze Chat with HelpCrunch

Updates a chat's snooze status in HelpCrunch.

## Endpoint

- **Method:** `PUT`
- **Path:** `/chats/snooze`
- **Base URL:** `https://api.helpcrunch.com/v1`
- **Official documentation:** [Snooze Chat](https://docs.helpcrunch.com/en/rest-api-v1/snooze-chat-v1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `number` | yes |
| `snoozedUntil` | body | `string` | yes |
