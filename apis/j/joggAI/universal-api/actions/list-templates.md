# JoggAI: List Templates



```
GET https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JoggAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/list-templates?${params}`, {
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
      "aspectRatio": 1,
      "coverUrl": "https://example.com",
      "id": 1,
      "name": "Ava Chen",
      "previewUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aspectRatio` | number | Template aspect ratio code |
| `coverUrl` | string | Template cover image URL |
| `id` | number | Template ID |
| `name` | string | Template name |
| `previewUrl` | string | Template preview video URL |

## Native endpoint

Through the native JoggAI API, this operation is `GET /v2/templates/custom` (base URL `https://api.jogg.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

