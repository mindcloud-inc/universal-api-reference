# Recallai: Create Bot

Creates a new bot in Recallai.

```
POST https://connect.mindcloud.co/v1/universal/recallai/latest/actions/create-bot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recallai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/create-bot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "meetingUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recallai/latest/actions/create-bot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "meetingUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botName` | string | no | The name of the bot that will be displayed in the call. *(Note: Authenticated Google Meet bots will use the Google account name and this field will be ignored.)* |
| `joinAt` | string | no | The time at which the bot will join the call, formatted in ISO 8601. This field can only be read from scheduled bots that have not yet joined a call. |
| `meetingUrl` | string | yes | The url of the meeting. For example, https://zoom.us/j/123?pwd=456. This field will be cleared a few days after the bot has joined a call. |

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

Through the native Recallai API, this operation is `POST /api/v1/bot/` (base URL `https://{{credentials.workspaceRegion}}.recall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bot.md) for the provider-specific parameters and requirements.

