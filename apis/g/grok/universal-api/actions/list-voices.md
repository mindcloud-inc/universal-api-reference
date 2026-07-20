# Grok: List Voices

Retrieves a list of voices from Grok.

```
GET https://connect.mindcloud.co/v1/universal/grok/latest/actions/list-voices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grok/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grok/latest/actions/list-voices?${params}`, {
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
      "voices": [
        {
          "language": "string",
          "name": "Ava Chen",
          "voiceId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `voices` | array<object> | Voices available for text-to-speech. |
| `voices[].language` | string | Supported language for the voice. |
| `voices[].name` | string | Display name for the voice. |
| `voices[].voiceId` | string | Voice identifier. |

## Native endpoint

Through the native Grok API, this operation is `GET /v1/tts/voices` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-voices.md) for the provider-specific parameters and requirements.

