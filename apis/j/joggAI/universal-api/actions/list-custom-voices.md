# JoggAI: List Custom Voices



```
GET https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/list-custom-voices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JoggAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/list-custom-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/list-custom-voices?${params}`, {
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
      "audioUrl": "https://example.com",
      "language": "string",
      "name": "Ava Chen",
      "voiceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audioUrl` | string | Sample audio URL for the custom voice |
| `language` | string | Voice language |
| `name` | string | Custom voice name |
| `voiceId` | string | Custom voice identifier |

## Native endpoint

Through the native JoggAI API, this operation is `GET /v2/voices/custom` (base URL `https://api.jogg.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-voices.md) for the provider-specific parameters and requirements.

