# Gyazo: List Images

Retrieves images from Gyazo.

```
GET https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/list-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gyazo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/list-images?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/list-images?${params}`, {
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
| `page` | number | no | Page number. |
| `perPage` | number | no | Number of images to return, from 1 to 100. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "image_id": "string",
      "metadata": {},
      "permalink_url": "https://example.com",
      "thumb_url": "https://example.com",
      "type": "string",
      "url": "https://example.com"
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
| `permalink_url` | string |  |
| `thumb_url` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Gyazo API, this operation is `GET /api/images` (base URL `https://api.gyazo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-images.md) for the provider-specific parameters and requirements.

