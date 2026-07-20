# List Bot Steps with BotHelp

Retrieves step details for a bot in BotHelp.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/bots/:bot_referral/steps`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [List Bot Steps](https://main.bothelp.io/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_referral` | path | `string` | yes | Bot referral identifier from BotHelp. |
