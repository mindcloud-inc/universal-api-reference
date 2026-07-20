# Locu: Update Session Activity

Updates an existing session activity in Locu.

```
PUT https://connect.mindcloud.co/v1/universal/locu/latest/actions/update-session-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Locu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/locu/latest/actions/update-session-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "activityId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/locu/latest/actions/update-session-activity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "activityId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Session ID that owns the activity. |
| `activityId` | string | yes | Activity ID to update. |
| `createdAt` | date | no | New activity start timestamp in ISO 8601 format. |
| `finishedAt` | date | no | New activity end timestamp in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "finishedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isManual": true,
      "sessionId": "string",
      "taskId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `finishedAt` | date |  |
| `id` | string |  |
| `isManual` | boolean |  |
| `sessionId` | string |  |
| `taskId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Locu API, this operation is `PATCH /sessions/:id/activities/:activityId` (base URL `https://api.locu.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-session-activity.md) for the provider-specific parameters and requirements.

