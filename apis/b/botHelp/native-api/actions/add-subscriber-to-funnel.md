# Add Subscriber To Funnel with BotHelp

Adds a subscriber to a funnel in BotHelp.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/subscribers/:subscriber_id/funnel`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [Add Subscriber To Funnel](https://main.bothelp.io/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `funnelReferral` | body | `string` | yes | Sequence/funnel referral to add the subscriber to. |
| `subscriber_id` | path | `string` | yes | BotHelp subscriber ID. |
