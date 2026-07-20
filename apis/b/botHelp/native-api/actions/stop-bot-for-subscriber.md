# Stop Bot For Subscriber with BotHelp

Stops a bot for a subscriber in BotHelp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/subscribers/:subscriber_id/bot`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [Stop Bot For Subscriber](https://main.bothelp.io/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botReferral` | query | `string` | no | Optional bot referral to stop. |
| `subscriber_id` | path | `string` | yes | BotHelp subscriber ID. |
