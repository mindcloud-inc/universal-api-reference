# JoggAI: List Custom Avatars



```
GET https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/list-custom-avatars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JoggAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/list-custom-avatars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/list-custom-avatars?${params}`, {
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
      "apiOnly": true,
      "avatarStatus": "string",
      "avatarUrl": "https://example.com",
      "coverUrl": "https://example.com",
      "failMsg": "string",
      "id": 1,
      "name": "Ava Chen",
      "videoUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiOnly` | boolean | Whether the avatar is available only through the API |
| `avatarStatus` | string | Avatar generation status |
| `avatarUrl` | string | Generated avatar video URL |
| `coverUrl` | string | Avatar cover image URL |
| `failMsg` | string | Failure message when generation fails |
| `id` | number | Custom avatar ID |
| `name` | string | Custom avatar name |
| `videoUrl` | string | Source or preview video URL |

## Native endpoint

Through the native JoggAI API, this operation is `GET /v2/avatars/custom` (base URL `https://api.jogg.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-avatars.md) for the provider-specific parameters and requirements.

