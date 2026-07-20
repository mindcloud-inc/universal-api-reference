# Voicemaker: Update Voice Clone

Updates an existing voice clone in Voicemaker.

```
PUT https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/update-voice-clone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voicemaker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/update-voice-clone" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "voiceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/update-voice-clone', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "voiceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `voiceId` | string | yes | Voice clone ID to update. |
| `name` | string | no | Updated name for the voice clone. |
| `description` | string | no | Updated description for the voice clone. |
| `labels` | object | no | Updated labels object for the voice clone. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Voicemaker API, this operation is `PUT api/v1/voice-clones/{VoiceId}` (base URL `https://developer.voicemaker.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-voice-clone.md) for the provider-specific parameters and requirements.

