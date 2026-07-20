# Invidious: Get Video Annotations



```
GET https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-video-annotations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-video-annotations?connectionId=$CONNECTION_ID&id=dQw4w9WgXcQ" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "dQw4w9WgXcQ"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-video-annotations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Video ID to fetch annotations for. Example: `dQw4w9WgXcQ`. |
| `source` | string | no | Annotation source: archive or youtube. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "source": "string",
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `source` | string |  |
| `videoId` | string |  |

## Native endpoint

Through the native Invidious API, this operation is `GET /annotations/:id` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-annotations.md) for the provider-specific parameters and requirements.

