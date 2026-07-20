# LiveKit: Create Ingress

Creates a new ingress in LiveKit.

```
POST https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/create-ingress
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/create-ingress" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inputType": "string",
  "roomName": "Ava Chen",
  "participantIdentity": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/create-ingress', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inputType": "string",
    "roomName": "Ava Chen",
    "participantIdentity": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inputType` | string | yes | Ingress input type, such as RTMP_INPUT, WHIP_INPUT, or URL_INPUT. |
| `name` | string | no |  |
| `roomName` | string | yes |  |
| `participantIdentity` | string | yes |  |
| `participantName` | string | no |  |
| `enableTranscoding` | boolean | no | For RTMP_INPUT, LiveKit requires transcoding to be enabled. Set false only for input types/configurations that support bypassing transcoding. Default: `true`. |
| `url` | string | no | HTTP, HLS, MP4, MOV, MKV, OGG, MP3, M4A, or SRT URL for URL_INPUT ingress. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audio": {},
      "bypass_transcoding": true,
      "enable_transcoding": true,
      "ingress_id": "string",
      "input_type": "string",
      "name": "Ava Chen",
      "participant_identity": "string",
      "participant_metadata": "string",
      "participant_name": "Ava Chen",
      "reusable": true,
      "room_name": "Ava Chen",
      "state": {},
      "stream_key": "string",
      "url": "https://example.com",
      "video": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audio` | object | Ingress audio settings. |
| `bypass_transcoding` | boolean | Whether transcoding is bypassed. |
| `enable_transcoding` | boolean | Whether transcoding is enabled. |
| `ingress_id` | string | LiveKit ingress ID. |
| `input_type` | string | Ingress input type. |
| `name` | string | Ingress name. |
| `participant_identity` | string | Participant identity used by the ingress. |
| `participant_metadata` | string | Participant metadata. |
| `participant_name` | string | Participant display name. |
| `reusable` | boolean | Whether the ingress can be reused. |
| `room_name` | string | Target room name. |
| `state` | object | Ingress runtime state. |
| `stream_key` | string | Generated RTMP stream key. |
| `url` | string | Ingress ingest URL. |
| `video` | object | Ingress video settings. |

## Native endpoint

Through the native LiveKit API, this operation is `POST /twirp/livekit.Ingress/CreateIngress` (base URL `{{credentials.livekitUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ingress.md) for the provider-specific parameters and requirements.

