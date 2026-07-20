# Add Subscriber To Funnel By CUID with BotHelp

Adds a subscriber to a funnel by CUID in BotHelp.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/subscribers/cuid/:subscriber_cuid/funnel`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [Add Subscriber To Funnel By CUID](https://main.bothelp.io/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `funnelReferral` | body | `string` | yes | Sequence/funnel referral to add the subscriber to. |
| `subscriber_cuid` | path | `string` | yes | BotHelp subscriber CUID. |
