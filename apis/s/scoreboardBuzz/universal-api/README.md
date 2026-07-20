# <img src="https://images.mindcloud.co/apps/icons/scoreboard-buzz_1774990453108.png" alt="Scoreboard Buzz logo" width="28" height="28"> Scoreboard Buzz: Universal API

Track activities, manage games, and score team performance

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scoreboardBuzz/latest
- **Category:** Productivity / Project Management
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.scoreboardbuzz.com/
- **Vendor API docs:** https://docs.scoreboardbuzz.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Recent Activities](actions/list-recent-activities.md) | GET | Retrieves recent activities from Scoreboard Buzz. |
| [Score Activities](actions/score-activities.md) | POST | Creates scored activities in Scoreboard Buzz in one request. |

### Game

| Action | Method | Description |
| --- | --- | --- |
| [Get Game Payload](actions/get-game-payload.md) | GET | Retrieves a game payload from Scoreboard Buzz. |
| [List Games](actions/list-games.md) | GET | Retrieves games from Scoreboard Buzz. |
| [List Recent Game Ended Events](actions/list-recent-game-ended-events.md) | GET | Retrieves recent game-ended events from Scoreboard Buzz. |

### Trackable

| Action | Method | Description |
| --- | --- | --- |
| [List Trackables](actions/list-trackables.md) | GET | Retrieves trackables from Scoreboard Buzz. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from Scoreboard Buzz. |
| [Register User With Knock](actions/register-user-with-knock.md) | POST | Creates a Knock registration for the authenticated user in Scoreboard Buzz. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST | Creates a webhook subscription in Scoreboard Buzz. |
| [Remove Webhook Subscription](actions/remove-webhook-subscription.md) | DELETE | Deletes a webhook subscription from Scoreboard Buzz. |

### Webhook Subscription

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | GET | Retrieves webhook subscriptions from Scoreboard Buzz. |

