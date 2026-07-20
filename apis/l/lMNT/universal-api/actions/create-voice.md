# LMNT: Create Voice

Creates a new voice in LMNT.

```
POST https://connect.mindcloud.co/v1/universal/lMNT/latest/actions/create-voice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LMNT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lMNT/latest/actions/create-voice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "enhance": true,
  "files": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lMNT/latest/actions/create-voice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "enhance": true,
    "files": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Optional description for the new voice. |
| `enhance` | boolean | yes | Whether LMNT should apply enhancement to noisy source audio. |
| `files` | file | yes | One or more training audio files in wav, mp3, mp4, m4a, or webm format. Accepts multiple values as an array. |
| `gender` | string | no | Optional gender tag such as male, female, or nonbinary. |
| `name` | string | yes | The display name for the new voice. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gender": "string",
      "id": "string",
      "name": "Ava Chen",
      "owner": "string",
      "preview_url": "https://example.com",
      "starred": true,
      "state": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gender` | string |  |
| `id` | string |  |
| `name` | string |  |
| `owner` | string |  |
| `preview_url` | string |  |
| `starred` | boolean |  |
| `state` | string |  |
| `type` | string |  |

## Native endpoint

Through the native LMNT API, this operation is `POST /v1/ai/voice` (base URL `https://api.lmnt.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-voice.md) for the provider-specific parameters and requirements.

