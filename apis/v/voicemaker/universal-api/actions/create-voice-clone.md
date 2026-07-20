# Voicemaker: Create Voice Clone

Creates a new voice clone in Voicemaker.

```
POST https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/create-voice-clone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voicemaker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/create-voice-clone" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "files": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/create-voice-clone', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "files": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Display name for the new voice clone. |
| `files` | file | yes | One or more MP3, WAV, or MP4 audio samples for the clone. Accepts multiple values as an array. |
| `description` | string | no | Optional description for the voice clone. |
| `removeBackground` | boolean | no | Whether to remove background noise from the uploaded samples. |
| `labels` | object | no | JSON labels object such as category, accent, gender, and age. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true,
      "voiceClone": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `success` | boolean |  |
| `voiceClone` | object |  |

## Native endpoint

Through the native Voicemaker API, this operation is `POST api/v1/voice-clones/add` (base URL `https://developer.voicemaker.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-voice-clone.md) for the provider-specific parameters and requirements.

