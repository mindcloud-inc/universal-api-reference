# Twitch: Delete Channel Stream Schedule Segment

Deletes a stream schedule segment from Twitch.

```
DELETE https://connect.mindcloud.co/v1/universal/twitch/latest/actions/delete-channel-stream-schedule-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/delete-channel-stream-schedule-segment?connectionId=$CONNECTION_ID&broadcasterId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "broadcasterId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twitch/latest/actions/delete-channel-stream-schedule-segment?${params}`, {
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
| `broadcasterId` | string | yes | The ID of the broadcaster that owns the streaming schedule. |
| `id` | string | yes | The ID of the broadcast segment to remove. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Empty response body returned when the stream schedule segment is deleted successfully. |

## Native endpoint

Through the native Twitch API, this operation is `DELETE /schedule/segment` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-channel-stream-schedule-segment.md) for the provider-specific parameters and requirements.

