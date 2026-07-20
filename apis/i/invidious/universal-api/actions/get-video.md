# Invidious: Get Video



```
GET https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-video?connectionId=$CONNECTION_ID&id=dQw4w9WgXcQ" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "dQw4w9WgXcQ"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-video?${params}`, {
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
| `id` | string | yes | YouTube/Invidious video ID. Example: `dQw4w9WgXcQ`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `region` | string | no | ISO 3166 country code. Example: `US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "authorId": "string",
      "keywords": [
        "string"
      ],
      "lengthSeconds": 1,
      "publishedText": "string",
      "title": "string",
      "videoId": "string",
      "viewCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `authorId` | string |  |
| `keywords` | array<string> |  |
| `lengthSeconds` | number |  |
| `publishedText` | string |  |
| `title` | string |  |
| `videoId` | string |  |
| `viewCount` | number |  |

## Native endpoint

Through the native Invidious API, this operation is `GET /videos/:id` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video.md) for the provider-specific parameters and requirements.

