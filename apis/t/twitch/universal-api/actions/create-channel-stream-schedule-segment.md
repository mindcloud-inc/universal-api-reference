# Twitch: Create Channel Stream Schedule Segment

Creates a stream schedule segment in Twitch.

```
POST https://connect.mindcloud.co/v1/universal/twitch/latest/actions/create-channel-stream-schedule-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/create-channel-stream-schedule-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "broadcasterId": "string",
  "startTime": "string",
  "timezone": "string",
  "duration": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twitch/latest/actions/create-channel-stream-schedule-segment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "broadcasterId": "string",
    "startTime": "string",
    "timezone": "string",
    "duration": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `broadcasterId` | string | yes | The broadcaster whose schedule to update. This ID must match the user ID in the access token. |
| `startTime` | string | yes | RFC3339 timestamp for the scheduled segment, for example 2026-03-13T18:30:00Z. |
| `timezone` | list | yes | IANA time zone where the broadcast takes place. |
| `duration` | number | yes | Scheduled length in minutes. Twitch requires a value from 30 through 1380. |
| `isRecurring` | boolean | no | Whether the broadcast recurs weekly. |
| `categoryId` | string | no | Category/game ID that best represents the broadcast content. |
| `title` | string | no | Broadcast title. Maximum 140 characters. |

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
          "endTime": {},
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
| `segments[].endTime` | object |  |
| `segments[].id` | string |  |
| `segments[].isRecurring` | boolean |  |
| `segments[].startTime` | string |  |
| `segments[].title` | string |  |
| `vacation` | object |  |

## Native endpoint

Through the native Twitch API, this operation is `POST /schedule/segment` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-channel-stream-schedule-segment.md) for the provider-specific parameters and requirements.

