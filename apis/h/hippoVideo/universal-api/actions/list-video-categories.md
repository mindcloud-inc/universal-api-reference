# Hippo Video: List Video Categories

Retrieves video categories from Hippo Video.

```
GET https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/list-video-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hippo Video `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/list-video-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/list-video-categories?${params}`, {
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
      "categories": [
        [
          {}
        ]
      ],
      "code": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories[]` | array<object> |  |
| `categories[].createdAt` | string |  |
| `categories[].createdBy` | string |  |
| `categories[].id` | number |  |
| `categories[].name` | string |  |
| `categories[].numVideos` | number |  |
| `code` | number |  |

## Native endpoint

Through the native Hippo Video API, this operation is `GET /api/v1/me/video/categories` (base URL `https://www.hippovideo.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-video-categories.md) for the provider-specific parameters and requirements.

