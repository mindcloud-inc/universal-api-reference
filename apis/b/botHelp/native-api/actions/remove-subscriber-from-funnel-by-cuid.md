# Remove Subscriber From Funnel By CUID with BotHelp

Removes a subscriber from a funnel by CUID in BotHelp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/subscribers/cuid/:subscriber_cuid/funnel`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [Remove Subscriber From Funnel By CUID](https://main.bothelp.io/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `funnelReferral` | query | `string` | no | Optional sequence/funnel referral to remove. |
| `subscriber_cuid` | path | `string` | yes | BotHelp subscriber CUID. |
