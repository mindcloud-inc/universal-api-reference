# Meetstream AI: Reschedule Bot

Updates a scheduled bot in Meetstream AI.

```
PUT https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/reschedule-bot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meetstream AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/reschedule-bot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": "string",
  "scheduledJoinTime": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/reschedule-bot', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": "string",
    "scheduledJoinTime": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | string | yes | The scheduled bot identifier. |
| `scheduledJoinTime` | date | yes | The new scheduled join time in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "botId": "string",
      "message": "string",
      "scheduleUpdated": true,
      "updatedFields": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botId` | string | Scheduled bot identifier. |
| `message` | string | Result message from the schedule update. |
| `scheduleUpdated` | boolean | Whether the schedule was updated. |
| `updatedFields` | array<string> | Fields updated by the reschedule call. |

## Native endpoint

Through the native Meetstream AI API, this operation is `PATCH /calendar/scheduled_bots/:bot_id` (base URL `https://api.meetstream.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reschedule-bot.md) for the provider-specific parameters and requirements.

