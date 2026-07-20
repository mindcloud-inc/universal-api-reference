# JoggAI: List Voices



```
GET https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/list-voices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JoggAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/list-voices?${params}`, {
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
      "audioUrl": "https://example.com",
      "gender": "string",
      "language": "string",
      "name": "Ava Chen",
      "useCase": "string",
      "voiceId": "string"
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
| `audioUrl` | string |  |
| `gender` | string |  |
| `language` | string |  |
| `name` | string |  |
| `useCase` | string |  |
| `voiceId` | string |  |

## Native endpoint

Through the native JoggAI API, this operation is `GET /v2/voices` (base URL `https://api.jogg.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-voices.md) for the provider-specific parameters and requirements.

