# Scoreboard Buzz: List Recent Game Ended Events

Retrieves recent game-ended events from Scoreboard Buzz.

```
GET https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/list-recent-game-ended-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoreboard Buzz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/list-recent-game-ended-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/list-recent-game-ended-events?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": 1,
      "event_type": "string",
      "game_id": 1,
      "game_name": "Ava Chen",
      "id": "string",
      "period_end": "2026-05-07T12:00:00.000Z",
      "period_start": "2026-05-07T12:00:00.000Z",
      "triggered_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number | Account ID associated with the event. |
| `event_type` | string | Webhook event type. |
| `game_id` | number | Game ID associated with the event. |
| `game_name` | string | Game name associated with the event. |
| `id` | string | Recent game-ended event ID. |
| `period_end` | date | End date of the completed scoring period. |
| `period_start` | date | Start date of the completed scoring period. |
| `triggered_at` | date | Timestamp when the event was triggered. |

## Native endpoint

Through the native Scoreboard Buzz API, this operation is `GET /webhooks/game-ended/recent` (base URL `https://api.scoreboardbuzz.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recent-game-ended-events.md) for the provider-specific parameters and requirements.

