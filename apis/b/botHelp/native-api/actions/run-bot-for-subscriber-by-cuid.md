# Run Bot For Subscriber By CUID with BotHelp

Runs a bot for a subscriber by CUID in BotHelp.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/subscribers/cuid/:subscriber_cuid/bot`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [Run Bot For Subscriber By CUID](https://main.bothelp.io/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botReferral` | body | `string` | yes | Bot referral to start for the subscriber. |
| `stepReferral` | body | `string` | no | Optional bot step referral to start at a specific step. |
| `subscriber_cuid` | path | `string` | yes | BotHelp subscriber CUID. |
