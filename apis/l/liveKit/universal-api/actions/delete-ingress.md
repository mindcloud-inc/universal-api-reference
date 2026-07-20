# LiveKit: Delete Ingress

Deletes an existing ingress from LiveKit.

```
DELETE https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/delete-ingress
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/delete-ingress?connectionId=$CONNECTION_ID&ingressId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ingressId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/delete-ingress?${params}`, {
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
| `ingressId` | string | yes |  |

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

Through the native LiveKit API, this operation is `POST /twirp/livekit.Ingress/DeleteIngress` (base URL `{{credentials.livekitUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-ingress.md) for the provider-specific parameters and requirements.

