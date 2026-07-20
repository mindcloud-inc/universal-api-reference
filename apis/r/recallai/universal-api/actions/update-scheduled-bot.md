# Recallai: Update Scheduled Bot

Updates a scheduled bot in Recallai.

```
PUT https://connect.mindcloud.co/v1/universal/recallai/latest/actions/update-scheduled-bot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recallai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/update-scheduled-bot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recallai/latest/actions/update-scheduled-bot', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | string | yes | A UUID string identifying this bot. |
| `botName` | string | no | The name of the bot that will be displayed in the call. *(Note: Authenticated Google Meet bots will use the Google account name and this field will be ignored.)* |
| `joinAt` | string | no | The time at which the bot will join the call, formatted in ISO 8601. This field can only be read from scheduled bots that have not yet joined a call. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "automaticLeave": {},
      "botName": "Ava Chen",
      "calendarMeetings": [
        "string"
      ],
      "id": "string",
      "joinAt": "string",
      "meetingUrl": {},
      "metadata": {},
      "recordingConfig": {},
      "recordings": [
        "string"
      ],
      "statusChanges": [
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
| `automaticLeave` | object |  |
| `botName` | string |  |
| `calendarMeetings` | array |  |
| `id` | string |  |
| `joinAt` | string |  |
| `meetingUrl` | object |  |
| `metadata` | object |  |
| `recordingConfig` | object |  |
| `recordings` | array |  |
| `statusChanges` | array |  |

## Native endpoint

Through the native Recallai API, this operation is `PATCH /api/v1/bot/:id/` (base URL `https://{{credentials.workspaceRegion}}.recall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-scheduled-bot.md) for the provider-specific parameters and requirements.

