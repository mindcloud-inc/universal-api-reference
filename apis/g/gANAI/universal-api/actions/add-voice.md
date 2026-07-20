# GAN.AI: Add Voice

Creates a custom voice in GAN.AI.

```
POST https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/add-voice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/add-voice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/add-voice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes |  |
| `voiceDescription` | string | no |  |
| `voiceName` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "voiceDescription": "string",
      "voiceId": "string",
      "voiceName": "Ava Chen",
      "voiceSample": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `voiceDescription` | string |  |
| `voiceId` | string |  |
| `voiceName` | string |  |
| `voiceSample` | string |  |

## Native endpoint

Through the native GAN.AI API, this operation is `POST /v1/voices` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-voice.md) for the provider-specific parameters and requirements.

