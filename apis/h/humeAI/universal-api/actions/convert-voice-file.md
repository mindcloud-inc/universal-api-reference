# Hume AI: Convert Voice File

Converts uploaded audio in Hume AI and returns a streamed audio file.

```
POST https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/convert-voice-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hume AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/convert-voice-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audio": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/convert-voice-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audio": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audio` | file | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Audio bytes. |
| `type` | string | Serialized buffer marker. |

## Native endpoint

Through the native Hume AI API, this operation is `POST /v0/tts/voice_conversion/file` (base URL `https://api.hume.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-voice-file.md) for the provider-specific parameters and requirements.

