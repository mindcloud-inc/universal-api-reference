# Trint: Create Push Stream

Creates a new push stream in Trint.

```
POST https://connect.mindcloud.co/v1/universal/trint/latest/actions/create-push-stream
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trint/latest/actions/create-push-stream" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trint/latest/actions/create-push-stream', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "streamKey": "string",
      "streamUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `streamKey` | string | Generated stream key for the realtime feed. |
| `streamUrl` | string | Generated RTMP stream URL for the realtime feed. |

## Native endpoint

Through the native Trint API, this operation is `POST /transcripts/realtime/push` (base URL `https://api.trint.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-push-stream.md) for the provider-specific parameters and requirements.

