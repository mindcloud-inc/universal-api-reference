# JoggAI: List Public Avatars



```
GET https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/list-public-avatars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JoggAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/list-public-avatars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/list-public-avatars?${params}`, {
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
      "age": "string",
      "aspectRatio": 1,
      "coverUrl": "https://example.com",
      "gender": "string",
      "id": 1,
      "name": "Ava Chen",
      "style": "string",
      "videoUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `age` | string |  |
| `aspectRatio` | number |  |
| `coverUrl` | string |  |
| `gender` | string |  |
| `id` | number |  |
| `name` | string |  |
| `style` | string |  |
| `videoUrl` | string |  |

## Native endpoint

Through the native JoggAI API, this operation is `GET /v2/avatars/public` (base URL `https://api.jogg.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-public-avatars.md) for the provider-specific parameters and requirements.

