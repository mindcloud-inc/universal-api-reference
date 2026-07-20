# CAMB.AI: Create Custom Voice

Creates a new custom voice in CAMB.AI.

```
POST https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/create-custom-voice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CAMB.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/create-custom-voice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "voiceName": "Ava Chen",
  "gender": 1,
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/create-custom-voice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "voiceName": "Ava Chen",
    "gender": 1,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `voiceName` | string | yes | Name to assign to the custom voice. |
| `gender` | number | yes | Gender code for the custom voice sample. |
| `file` | file | yes | Reference audio file used to create the custom voice. |
| `description` | string | no | Optional summary of the custom voice and its intended use. |
| `age` | number | no | Estimated or actual age of the speaker in the reference audio. |
| `enhanceAudio` | boolean | no | Whether CAMB.AI should enhance the uploaded sample before cloning. |
| `language` | number | no | Optional numeric language identifier for the reference audio. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "voice_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `voice_id` | number | Identifier of the newly created custom voice. |

## Native endpoint

Through the native CAMB.AI API, this operation is `POST /create-custom-voice` (base URL `https://client.camb.ai/apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-voice.md) for the provider-specific parameters and requirements.

