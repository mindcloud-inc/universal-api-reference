# BotHelp: Native API Reference

A consolidated summary of BotHelp's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://help.bothelp.io/en/api-bothelp/
- **API base URL:** `https://api.bothelp.io`

## Authentication

### Bearer Token

Use a BotHelp bearer token obtained from the official client_credentials token endpoint.

### Credentials

- **Access Token:** `accessToken` · required · BotHelp bearer token obtained from https://oauth.bothelp.io/oauth2/token using client_credentials.

Send these headers with each API request:

```http
Authorization: Bearer <accessToken>
```

[Official authentication documentation](https://help.bothelp.io/en/api-bothelp/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Filtering

Send filters in the query string.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Messenger Subscriber To Funnel](actions/add-messenger-subscriber-to-funnel.md) | `POST /v2/subscribers/messenger/:messenger_user_id/funnel` | [docs](https://main.bothelp.io/swagger) |
| [Add Subscriber To Funnel](actions/add-subscriber-to-funnel.md) | `POST /v1/subscribers/:subscriber_id/funnel` | [docs](https://main.bothelp.io/swagger) |
| [Add Subscriber To Funnel By CUID](actions/add-subscriber-to-funnel-by-cuid.md) | `POST /v1/subscribers/cuid/:subscriber_cuid/funnel` | [docs](https://main.bothelp.io/swagger) |
| [List Bot Steps](actions/list-bot-steps.md) | `GET /v1/bots/:bot_referral/steps` | [docs](https://main.bothelp.io/swagger) |
| [List Bots](actions/list-bots.md) | `GET /v1/bots/` | [docs](https://main.bothelp.io/swagger) |
| [List Funnels](actions/list-funnels.md) | `GET /v1/funnels/` | [docs](https://main.bothelp.io/swagger) |
| [List Subscribers](actions/list-subscribers.md) | `GET /v1/subscribers/` | [docs](https://main.bothelp.io/swagger) |
| [Remove Messenger Subscriber From Funnel](actions/remove-messenger-subscriber-from-funnel.md) | `DELETE /v2/subscribers/messenger/:messenger_user_id/funnel` | [docs](https://main.bothelp.io/swagger) |
| [Remove Subscriber From Funnel](actions/remove-subscriber-from-funnel.md) | `DELETE /v1/subscribers/:subscriber_id/funnel` | [docs](https://main.bothelp.io/swagger) |
| [Remove Subscriber From Funnel By CUID](actions/remove-subscriber-from-funnel-by-cuid.md) | `DELETE /v1/subscribers/cuid/:subscriber_cuid/funnel` | [docs](https://main.bothelp.io/swagger) |
| [Run Bot For Messenger Subscriber](actions/run-bot-for-messenger-subscriber.md) | `POST /v2/subscribers/messenger/:messenger_user_id/bot` | [docs](https://main.bothelp.io/swagger) |
| [Run Bot For Subscriber](actions/run-bot-for-subscriber.md) | `POST /v1/subscribers/:subscriber_id/bot` | [docs](https://main.bothelp.io/swagger) |
| [Run Bot For Subscriber By CUID](actions/run-bot-for-subscriber-by-cuid.md) | `POST /v1/subscribers/cuid/:subscriber_cuid/bot` | [docs](https://main.bothelp.io/swagger) |
| [Send Subscriber Message](actions/send-subscriber-message.md) | `POST /v1/subscribers/:subscriber_id/messages` | [docs](https://main.bothelp.io/swagger) |
| [Send Subscriber Message By CUID](actions/send-subscriber-message-by-cuid.md) | `POST /v1/subscribers/cuid/:subscriber_cuid/messages` | [docs](https://main.bothelp.io/swagger) |
| [Stop Bot For Messenger Subscriber](actions/stop-bot-for-messenger-subscriber.md) | `DELETE /v2/subscribers/messenger/:messenger_user_id/bot` | [docs](https://main.bothelp.io/swagger) |
| [Stop Bot For Subscriber](actions/stop-bot-for-subscriber.md) | `DELETE /v1/subscribers/:subscriber_id/bot` | [docs](https://main.bothelp.io/swagger) |
| [Stop Bot For Subscriber By CUID](actions/stop-bot-for-subscriber-by-cuid.md) | `DELETE /v1/subscribers/cuid/:subscriber_cuid/bot` | [docs](https://main.bothelp.io/swagger) |
| [Update Messenger Subscriber](actions/update-messenger-subscriber.md) | `PATCH /v2/subscribers/messenger/:messenger_user_id` | [docs](https://main.bothelp.io/swagger) |
| [Update Messenger Subscriber Custom Fields](actions/update-messenger-subscriber-custom-fields.md) | `PATCH /v2/subscribers/messenger/:messenger_user_id/custom-fields` | [docs](https://main.bothelp.io/swagger) |
| [Update Subscriber](actions/update-subscriber.md) | `PATCH /v1/subscribers/:subscriber_id` | [docs](https://main.bothelp.io/swagger) |
| [Update Subscriber By CUID](actions/update-subscriber-by-cuid.md) | `PATCH /v1/subscribers/cuid/:subscriber_cuid` | [docs](https://main.bothelp.io/swagger) |
| [Update Subscriber Custom Fields](actions/update-subscriber-custom-fields.md) | `PATCH /v1/subscribers/:subscriber_id/customFields` | [docs](https://main.bothelp.io/swagger) |
| [Update Subscriber Custom Fields By CUID](actions/update-subscriber-custom-fields-by-cuid.md) | `PATCH /v1/subscribers/cuid/:subscriber_cuid/customFields` | [docs](https://main.bothelp.io/swagger) |
