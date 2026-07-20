# Mux: Create Live Stream Simulcast Target



```
POST https://connect.mindcloud.co/v1/universal/mux/latest/actions/create-live-stream-simulcast-target
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mux/latest/actions/create-live-stream-simulcast-target" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "liveStreamId": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mux/latest/actions/create-live-stream-simulcast-target', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "liveStreamId": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `liveStreamId` | string | yes | The Mux live stream ID. |
| `url` | string | yes | The RTMP destination URL for the simulcast target. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native Mux API, this operation is `POST /video/v1/live-streams/{LIVE_STREAM_ID}/simulcast-targets` (base URL `https://api.mux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-live-stream-simulcast-target.md) for the provider-specific parameters and requirements.

