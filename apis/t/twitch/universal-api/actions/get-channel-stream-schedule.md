# Twitch: Get Channel Stream Schedule

Retrieves channel stream schedules from Twitch.

```
GET https://connect.mindcloud.co/v1/universal/twitch/latest/actions/get-channel-stream-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/get-channel-stream-schedule?connectionId=$CONNECTION_ID&broadcasterId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "broadcasterId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twitch/latest/actions/get-channel-stream-schedule?${params}`, {
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
| `broadcasterId` | string | yes | The ID of the broadcaster whose streaming schedule you want to get. |
| `id` | string | no | The ID of the scheduled segment to return. |
| `startTime` | date | no | A timestamp used to filter for segments that start on or after the specified UTC date and time. |
| `first` | number | no | The maximum number of segments to return. Maximum: 25. Default: 20. |

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

Through the native Twitch API, this operation is `GET /schedule` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel-stream-schedule.md) for the provider-specific parameters and requirements.

