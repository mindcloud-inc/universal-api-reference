# Gladia: Create Live Job

Creates a live transcription job in Gladia.

```
POST https://connect.mindcloud.co/v1/universal/gladia/latest/actions/create-live-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gladia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gladia/latest/actions/create-live-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gladia/latest/actions/create-live-job', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `encoding` | string | no | Audio encoding for the live stream. Match this to the audio chunks sent over the WebSocket. Default: `wav/pcm`. |
| `sampleRate` | number | no | Sample rate in Hz for the live audio stream. Default: `16000`. |
| `bitDepth` | number | no | Bit depth for the live audio stream. Default: `16`. |
| `channels` | number | no | Channel count for the live audio stream. Default: `1`. |
| `region` | list<string> | no | Optional region used to process the live audio stream. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Gladia API, this operation is `POST /v2/live` (base URL `https://api.gladia.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-live-job.md) for the provider-specific parameters and requirements.

