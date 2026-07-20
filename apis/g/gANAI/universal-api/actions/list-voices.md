# GAN.AI: List Voices

Retrieves available voice profiles from GAN.AI.

```
GET https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-voices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-voices?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native GAN.AI API, this operation is `GET /v1/voices` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-voices.md) for the provider-specific parameters and requirements.

