# Gyazo: Search Images

Finds images in Gyazo by search query.

```
GET https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/search-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gyazo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/search-images?connectionId=$CONNECTION_ID&query=invoice%20screenshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "invoice screenshot"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/search-images?${params}`, {
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
| `query` | string | yes | Search query text, maximum 200 characters. Example: `invoice screenshot`. |
| `page` | number | no | Page number. |
| `per` | number | no | Number of results per page, maximum 100. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "image_id": "string",
      "metadata": {},
      "mp4_url": "https://example.com",
      "ocr": {},
      "permalink_url": "https://example.com",
      "thumb_url": "https://example.com",
      "type": "string",
      "url": "https://example.com",
      "video_length": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `image_id` | string |  |
| `metadata` | object |  |
| `mp4_url` | string |  |
| `ocr` | object |  |
| `permalink_url` | string |  |
| `thumb_url` | string |  |
| `type` | string |  |
| `url` | string |  |
| `video_length` | number |  |

## Native endpoint

Through the native Gyazo API, this operation is `GET /api/search` (base URL `https://api.gyazo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-images.md) for the provider-specific parameters and requirements.

