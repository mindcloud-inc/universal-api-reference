# Recallai: Get Bot

Retrieves a bot from Recallai.

```
GET https://connect.mindcloud.co/v1/universal/recallai/latest/actions/get-bot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recallai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/get-bot?connectionId=$CONNECTION_ID&botId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recallai/latest/actions/get-bot?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | string | yes | A UUID string identifying this bot. |

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

Through the native Recallai API, this operation is `GET /api/v1/bot/:id/` (base URL `https://{{credentials.workspaceRegion}}.recall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bot.md) for the provider-specific parameters and requirements.

