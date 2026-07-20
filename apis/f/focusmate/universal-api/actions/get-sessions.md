# Focusmate: Get Sessions

Retrieves your Focusmate sessions within a date range.

```
GET https://connect.mindcloud.co/v1/universal/focusmate/latest/actions/get-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Focusmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/focusmate/latest/actions/get-sessions?connectionId=$CONNECTION_ID&start=2026-04-01T00%3A00%3A00Z&end=2026-04-29T23%3A59%3A59Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start": "2026-04-01T00:00:00Z",
  "end": "2026-04-29T23:59:59Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/focusmate/latest/actions/get-sessions?${params}`, {
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
| `start` | date | yes | Lower limit for the date range as an ISO 8601 date-time with an offset or Z. Sessions partially within the range are included. The range must not exceed 1 year. Example: `2026-04-01T00:00:00Z`. |
| `end` | date | yes | Upper limit for the date range as an ISO 8601 date-time with an offset or Z. Sessions partially within the range are included. The range must not exceed 1 year. Example: `2026-04-29T23:59:59Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": 1,
      "sessionId": "string",
      "startTime": "2026-05-07T12:00:00.000Z",
      "users": {
        "activityType": "string",
        "completed": true,
        "isFavorite": true,
        "joinedAt": "2026-05-07T12:00:00.000Z",
        "preferences": {},
        "requestedAt": "2026-05-07T12:00:00.000Z",
        "sessionTitle": "string",
        "userId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration` | number | Session duration in milliseconds. |
| `sessionId` | string | Unique identifier for the Focusmate session. |
| `startTime` | date | Session start time in UTC. |
| `users` | array<object> | Users who participated in the session. The calling user is first. |
| `users.activityType` | string | Focusmate activity type for the participant. |
| `users.completed` | boolean | Whether the participant completed the session. |
| `users.isFavorite` | boolean | Current favorite status for the non-calling user when returned. |
| `users.joinedAt` | date | Time the participant joined the session, when available. |
| `users.preferences` | object | Participant session preferences such as quiet mode and favorite-partner preference. |
| `users.requestedAt` | date | Time the participant requested the session. |
| `users.sessionTitle` | string | Session title or task for the participant when available. |
| `users.userId` | string | Focusmate user ID for a participant. |

## Native endpoint

Through the native Focusmate API, this operation is `GET /sessions` (base URL `https://api.focusmate.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sessions.md) for the provider-specific parameters and requirements.

