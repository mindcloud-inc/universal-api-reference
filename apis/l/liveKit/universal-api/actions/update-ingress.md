# LiveKit: Update Ingress

Updates an existing ingress in LiveKit.

```
PUT https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/update-ingress
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/update-ingress" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ingressId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/update-ingress', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ingressId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ingressId` | string | yes |  |
| `name` | string | no |  |
| `roomName` | string | no |  |
| `participantIdentity` | string | no |  |
| `participantName` | string | no |  |

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

Through the native LiveKit API, this operation is `POST /twirp/livekit.Ingress/UpdateIngress` (base URL `{{credentials.livekitUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ingress.md) for the provider-specific parameters and requirements.

