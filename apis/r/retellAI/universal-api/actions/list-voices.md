# Retell AI: List Voices

Retrieves voices from Retell AI.

```
GET https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/list-voices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retell AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/list-voices?${params}`, {
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
      "accent": "string",
      "age": "string",
      "avatarUrl": "https://example.com",
      "gender": "string",
      "previewAudioUrl": "https://example.com",
      "provider": "string",
      "recommended": true,
      "standardVoiceType": "string",
      "voiceId": "string",
      "voiceName": "Ava Chen",
      "voiceType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accent` | string |  |
| `age` | string |  |
| `avatarUrl` | string |  |
| `gender` | string |  |
| `previewAudioUrl` | string |  |
| `provider` | string |  |
| `recommended` | boolean |  |
| `standardVoiceType` | string |  |
| `voiceId` | string |  |
| `voiceName` | string |  |
| `voiceType` | string |  |

## Native endpoint

Through the native Retell AI API, this operation is `GET /list-voices` (base URL `https://api.retellai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-voices.md) for the provider-specific parameters and requirements.

