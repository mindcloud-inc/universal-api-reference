# Run Bot For Subscriber with BotHelp

Runs a bot for a subscriber in BotHelp.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/subscribers/:subscriber_id/bot`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [Run Bot For Subscriber](https://main.bothelp.io/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botReferral` | body | `string` | yes | Bot referral to start for the subscriber. |
| `stepReferral` | body | `string` | no | Optional bot step referral to start at a specific step. |
| `subscriber_id` | path | `string` | yes | BotHelp subscriber ID. |
