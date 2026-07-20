# Remove Subscriber From Funnel with BotHelp

Removes a subscriber from a funnel in BotHelp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/subscribers/:subscriber_id/funnel`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [Remove Subscriber From Funnel](https://main.bothelp.io/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `funnelReferral` | query | `string` | no | Optional sequence/funnel referral to remove. |
| `subscriber_id` | path | `string` | yes | BotHelp subscriber ID. |
