# Remove Messenger Subscriber From Funnel with BotHelp

Removes a subscriber from a funnel by Facebook Messenger user ID in BotHelp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/subscribers/messenger/:messenger_user_id/funnel`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [Remove Messenger Subscriber From Funnel](https://main.bothelp.io/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `funnelReferral` | query | `string` | no | Optional sequence/funnel referral to remove. |
| `messenger_user_id` | path | `string` | yes | Facebook Messenger user PSID. |
