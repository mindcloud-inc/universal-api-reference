# Mux: Delete Live Stream Playback ID



```
DELETE https://connect.mindcloud.co/v1/universal/mux/latest/actions/delete-live-stream-playback-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mux/latest/actions/delete-live-stream-playback-id?connectionId=$CONNECTION_ID&liveStreamId=string&playbackId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "liveStreamId": "string",
  "playbackId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mux/latest/actions/delete-live-stream-playback-id?${params}`, {
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
| `liveStreamId` | string | yes | The Mux live stream ID. |
| `playbackId` | string | yes | The Mux playback ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Mux API, this operation is `DELETE /video/v1/live-streams/{LIVE_STREAM_ID}/playback-ids/{PLAYBACK_ID}` (base URL `https://api.mux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-live-stream-playback-id.md) for the provider-specific parameters and requirements.

