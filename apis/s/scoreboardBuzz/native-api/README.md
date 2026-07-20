# Scoreboard Buzz: Native API Reference

A consolidated summary of Scoreboard Buzz's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.scoreboardbuzz.com/
- **OpenAPI specification:** https://docs.scoreboardbuzz.com/openapi.yaml
- **API base URL:** `https://api.scoreboardbuzz.com/api/v1`

## Authentication

### API Key

Connect with a Scoreboard Buzz API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.scoreboardbuzz.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | `POST /webhooks/subscribe` | [docs](https://docs.scoreboardbuzz.com/#/Webhooks/createWebhookSubscription) |
| [Get Game Payload](actions/get-game-payload.md) | `GET /games/:gameId/payload` | [docs](https://docs.scoreboardbuzz.com/#/Games/getGamePayload) |
| [List Games](actions/list-games.md) | `GET /games` | [docs](https://docs.scoreboardbuzz.com/#/Games/listGames) |
| [List Recent Activities](actions/list-recent-activities.md) | `GET /activities` | [docs](https://docs.scoreboardbuzz.com/#/Activities/listActivities) |
| [List Recent Game Ended Events](actions/list-recent-game-ended-events.md) | `GET /webhooks/game-ended/recent` | [docs](https://docs.scoreboardbuzz.com/#/Webhooks/getRecentGameEndedEvents) |
| [List Trackables](actions/list-trackables.md) | `GET /trackables` | [docs](https://docs.scoreboardbuzz.com/#/Trackables/listTrackables) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://docs.scoreboardbuzz.com/#/Users/listUsers) |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | `GET /webhooks/subscriptions` | [docs](https://docs.scoreboardbuzz.com/#/Webhooks/listWebhookSubscriptions) |
| [Register User With Knock](actions/register-user-with-knock.md) | `POST /users/knock` | [docs](https://docs.scoreboardbuzz.com/#/Users/registerUserKnock) |
| [Remove Webhook Subscription](actions/remove-webhook-subscription.md) | `DELETE /webhooks/unsubscribe` | [docs](https://docs.scoreboardbuzz.com/#/Webhooks/deleteWebhookSubscription) |
| [Score Activities](actions/score-activities.md) | `POST /activities` | [docs](https://docs.scoreboardbuzz.com/#/Activities/createActivities) |
