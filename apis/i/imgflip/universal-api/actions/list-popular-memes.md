# Imgflip: List Popular Memes



```
GET https://connect.mindcloud.co/v1/universal/imgflip/latest/actions/list-popular-memes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Imgflip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imgflip/latest/actions/list-popular-memes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imgflip/latest/actions/list-popular-memes?${params}`, {
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
| `type` | list | no | Optional type: image, gif, or the documented comma-separated combination such as gif,image. Defaults to image. One of: `gif`, `gif,image`, `image`. Default: `image`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "box_count": 1,
      "captions": 1,
      "height": 1,
      "id": "string",
      "name": "Ava Chen",
      "url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `box_count` | number | Default caption-box count. |
| `captions` | number | Estimated all-time captions. |
| `height` | number | Template height in pixels. |
| `id` | string | Imgflip template ID. |
| `name` | string | Template name. |
| `url` | string | Template image URL. |
| `width` | number | Template width in pixels. |

## Native endpoint

Through the native Imgflip API, this operation is `GET /get_memes` (base URL `https://api.imgflip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-popular-memes.md) for the provider-specific parameters and requirements.

