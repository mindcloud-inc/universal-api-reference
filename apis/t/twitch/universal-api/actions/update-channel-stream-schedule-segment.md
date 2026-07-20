# Twitch: Update Channel Stream Schedule Segment

Updates a stream schedule segment in Twitch.

```
PUT https://connect.mindcloud.co/v1/universal/twitch/latest/actions/update-channel-stream-schedule-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/update-channel-stream-schedule-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "broadcasterId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twitch/latest/actions/update-channel-stream-schedule-segment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "broadcasterId": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `broadcasterId` | string | yes | The ID of the broadcaster who owns the broadcast segment. |
| `id` | string | yes | The ID of the broadcast segment to update. |
| `startTime` | string | no | The date and time that the broadcast segment starts in RFC3339 format. |
| `duration` | number | no | The length of time, in minutes, that the broadcast is scheduled to run. |
| `categoryId` | string | no | The ID of the category that best represents the broadcast’s content. |
| `title` | string | no | The broadcast segment title. |
| `isCanceled` | boolean | no | Whether to cancel the scheduled segment. |
| `timezone` | list | no | The IANA time zone where the broadcast takes place. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "broadcasterId": "string",
      "broadcasterLogin": "string",
      "broadcasterName": "Ava Chen",
      "segments": [
        {
          "canceledUntil": {},
          "category": {},
          "endTime": "string",
          "id": "string",
          "isRecurring": true,
          "startTime": "string",
          "title": "string"
        }
      ],
      "vacation": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `broadcasterId` | string |  |
| `broadcasterLogin` | string |  |
| `broadcasterName` | string |  |
| `segments[].canceledUntil` | object |  |
| `segments[].category` | object |  |
| `segments[].endTime` | string |  |
| `segments[].id` | string |  |
| `segments[].isRecurring` | boolean |  |
| `segments[].startTime` | string |  |
| `segments[].title` | string |  |
| `vacation` | object |  |

## Native endpoint

Through the native Twitch API, this operation is `PATCH /schedule/segment` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-channel-stream-schedule-segment.md) for the provider-specific parameters and requirements.

