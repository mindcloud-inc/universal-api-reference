# Hedy: Get Session Details

Retrieves a session from Hedy.

```
GET https://connect.mindcloud.co/v1/universal/hedy/latest/actions/get-session-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hedy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hedy/latest/actions/get-session-details?connectionId=$CONNECTION_ID&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hedy/latest/actions/get-session-details?${params}`, {
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
| `sessionId` | string | yes | Unique identifier of the session. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cleanedAt": "2026-05-07T12:00:00.000Z",
      "cleanedTranscript": "string",
      "conversations": "string",
      "duration": 1,
      "endTime": "2026-05-07T12:00:00.000Z",
      "highlights": [
        {}
      ],
      "meetingMinutes": "string",
      "recap": "string",
      "sessionId": "string",
      "startTime": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "transcript": "string",
      "userTodos": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cleanedAt` | date |  |
| `cleanedTranscript` | string |  |
| `conversations` | string |  |
| `duration` | number |  |
| `endTime` | date |  |
| `highlights` | array<object> |  |
| `meetingMinutes` | string |  |
| `recap` | string |  |
| `sessionId` | string |  |
| `startTime` | date |  |
| `title` | string |  |
| `transcript` | string |  |
| `userTodos` | array<object> |  |

## Native endpoint

Through the native Hedy API, this operation is `GET https://api.hedy.bot/sessions/:sessionId` (base URL `https://api.hedy.bot`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session-details.md) for the provider-specific parameters and requirements.

