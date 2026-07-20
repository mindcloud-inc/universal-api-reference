# <img src="https://images.mindcloud.co/apps/icons/bot-help-icon_1776709316193.png" alt="BotHelp logo" width="28" height="28"> BotHelp: Universal API

Build BotHelp integrations for subscribers, flows, sequences, bot steps, custom fields, tags, and outbound messages through the official BotHelp Open API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/botHelp/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bothelp.io
- **Vendor API docs:** https://help.bothelp.io/en/api-bothelp/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Bots](actions/list-bots.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/list-bots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Bot

| Action | Method | Description |
| --- | --- | --- |
| [List Bots](actions/list-bots.md) | GET | Retrieves active bot details from BotHelp. |

### Funnel

| Action | Method | Description |
| --- | --- | --- |
| [List Funnels](actions/list-funnels.md) | GET | Retrieves active funnel details from BotHelp. |

### Step

| Action | Method | Description |
| --- | --- | --- |
| [List Bot Steps](actions/list-bot-steps.md) | GET | Retrieves step details for a bot in BotHelp. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Add Messenger Subscriber To Funnel](actions/add-messenger-subscriber-to-funnel.md) | PUT | Adds a subscriber to a funnel by Facebook Messenger user ID in BotHelp. |
| [Add Subscriber To Funnel](actions/add-subscriber-to-funnel.md) | PUT | Adds a subscriber to a funnel in BotHelp. |
| [Add Subscriber To Funnel By CUID](actions/add-subscriber-to-funnel-by-cuid.md) | PUT | Adds a subscriber to a funnel by CUID in BotHelp. |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves subscriber records from BotHelp. |
| [Remove Messenger Subscriber From Funnel](actions/remove-messenger-subscriber-from-funnel.md) | PUT | Removes a subscriber from a funnel by Facebook Messenger user ID in BotHelp. |
| [Remove Subscriber From Funnel](actions/remove-subscriber-from-funnel.md) | PUT | Removes a subscriber from a funnel in BotHelp. |
| [Remove Subscriber From Funnel By CUID](actions/remove-subscriber-from-funnel-by-cuid.md) | PUT | Removes a subscriber from a funnel by CUID in BotHelp. |
| [Run Bot For Messenger Subscriber](actions/run-bot-for-messenger-subscriber.md) | PUT | Runs a bot for a subscriber by Facebook Messenger user ID in BotHelp. |
| [Run Bot For Subscriber](actions/run-bot-for-subscriber.md) | PUT | Runs a bot for a subscriber in BotHelp. |
| [Run Bot For Subscriber By CUID](actions/run-bot-for-subscriber-by-cuid.md) | PUT | Runs a bot for a subscriber by CUID in BotHelp. |
| [Send Subscriber Message](actions/send-subscriber-message.md) | PUT | Sends a message to a subscriber in BotHelp. |
| [Send Subscriber Message By CUID](actions/send-subscriber-message-by-cuid.md) | PUT | Sends a message to a subscriber by CUID in BotHelp. |
| [Stop Bot For Messenger Subscriber](actions/stop-bot-for-messenger-subscriber.md) | PUT | Stops a bot for a subscriber by Facebook Messenger user ID in BotHelp. |
| [Stop Bot For Subscriber](actions/stop-bot-for-subscriber.md) | PUT | Stops a bot for a subscriber in BotHelp. |
| [Stop Bot For Subscriber By CUID](actions/stop-bot-for-subscriber-by-cuid.md) | PUT | Stops a bot for a subscriber by CUID in BotHelp. |
| [Update Messenger Subscriber](actions/update-messenger-subscriber.md) | PUT | Updates a subscriber by Facebook Messenger user ID in BotHelp. |
| [Update Messenger Subscriber Custom Fields](actions/update-messenger-subscriber-custom-fields.md) | PUT | Updates subscriber custom fields by Facebook Messenger user ID in BotHelp. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates an existing subscriber in BotHelp. |
| [Update Subscriber By CUID](actions/update-subscriber-by-cuid.md) | PUT | Updates a subscriber by CUID in BotHelp. |
| [Update Subscriber Custom Fields](actions/update-subscriber-custom-fields.md) | PUT | Updates subscriber custom fields in BotHelp. |
| [Update Subscriber Custom Fields By CUID](actions/update-subscriber-custom-fields-by-cuid.md) | PUT | Updates subscriber custom fields by CUID in BotHelp. |

