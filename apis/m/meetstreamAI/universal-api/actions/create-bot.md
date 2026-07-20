# Meetstream AI: Create Bot

Creates a new bot in Meetstream AI.

```
POST https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/create-bot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meetstream AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/create-bot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "meetingLink": "https://example.com",
  "botName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/create-bot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "meetingLink": "https://example.com",
    "botName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `meetingLink` | string | yes | The Google Meet, Zoom, or Teams meeting URL. |
| `botName` | string | yes | The display name the bot will use in the meeting. |
| `videoRequired` | boolean | no | Whether the bot should record video. Default: `true`. |
| `joinAt` | date | no | Schedule the bot to join at an ISO 8601 datetime. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botMessage` | string | no | Optional initial message for the bot to post in meeting chat. |
| `callbackUrl` | string | no | Optional webhook URL for event callbacks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "botId": "string",
      "joinAt": "string",
      "meetingUrl": "https://example.com",
      "scheduleName": "Ava Chen",
      "status": "string",
      "transcriptId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botId` | string | Created bot identifier. |
| `joinAt` | string | Scheduled join time returned by the API. |
| `meetingUrl` | string | Meeting URL associated with the bot. |
| `scheduleName` | string | Schedule name returned for scheduled bots. |
| `status` | string | Current bot status. |
| `transcriptId` | string | Transcript identifier when available. |

## Native endpoint

Through the native Meetstream AI API, this operation is `POST /bots/create_bot` (base URL `https://api.meetstream.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bot.md) for the provider-specific parameters and requirements.

