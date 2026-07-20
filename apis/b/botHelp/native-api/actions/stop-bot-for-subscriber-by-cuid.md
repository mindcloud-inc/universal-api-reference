# Stop Bot For Subscriber By CUID with BotHelp

Stops a bot for a subscriber by CUID in BotHelp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/subscribers/cuid/:subscriber_cuid/bot`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [Stop Bot For Subscriber By CUID](https://main.bothelp.io/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botReferral` | query | `string` | no | Optional bot referral to stop. |
| `subscriber_cuid` | path | `string` | yes | BotHelp subscriber CUID. |
