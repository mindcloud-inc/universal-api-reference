# Add Messenger Subscriber To Funnel with BotHelp

Adds a subscriber to a funnel by Facebook Messenger user ID in BotHelp.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/subscribers/messenger/:messenger_user_id/funnel`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [Add Messenger Subscriber To Funnel](https://main.bothelp.io/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `funnelReferral` | body | `string` | yes | Sequence/funnel referral to add the subscriber to. |
| `messenger_user_id` | path | `string` | yes | Facebook Messenger user PSID. |
