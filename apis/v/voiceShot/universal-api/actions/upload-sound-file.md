# VoiceShot: Upload Sound File

Creates a sound file in VoiceShot.

```
POST https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/upload-sound-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoiceShot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/upload-sound-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filename": "Ava Chen",
  "fileContentBase64": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/upload-sound-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filename": "Ava Chen",
    "fileContentBase64": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | string | yes | WAV filename to create in VoiceShot. |
| `fileContentBase64` | string | yes | Base64-encoded WAV file contents. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "errorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string | VoiceShot response comment or error message. |
| `errorId` | string | VoiceShot response error code. 0 means ok. |

## Native endpoint

Through the native VoiceShot API, this operation is `POST /ivrapi.asp` (base URL `https://api.voiceshot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-sound-file.md) for the provider-specific parameters and requirements.

