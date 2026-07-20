# VisionFly: List User Images

Retrieves user images from the VisionFly CDN.

```
GET https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/list-user-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VisionFly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/list-user-images?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/list-user-images?${params}`, {
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
| `cursor` | string | no | Pagination cursor from a previous response. |
| `limit` | string | no | Maximum number of images to return. |
| `project` | string | no | Optional project slug filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "images": [
        {}
      ],
      "nextCursor": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `images` | array<object> | Images matching the request. |
| `nextCursor` | string | Cursor for the next page, if any. |
| `total` | number | Total number of returned images. |

## Native endpoint

Through the native VisionFly API, this operation is `GET /cdn/images` (base URL `https://api.visionfly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-images.md) for the provider-specific parameters and requirements.

