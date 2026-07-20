# Hippo Video: List Videos

Retrieves videos from the Hippo Video library.

```
GET https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/list-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hippo Video `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/list-videos?connectionId=$CONNECTION_ID&page=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "page": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/list-videos?${params}`, {
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
| `page` | number | yes | Page number of the list |
| `categoryId` | number | no | ID of the category or folder |
| `videoType` | string | no | Type of video such as library or testimonial |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "hasNextPage": true,
      "page": 1,
      "videos": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `hasNextPage` | boolean |  |
| `page` | number |  |
| `videos[]` | array<object> |  |
| `videos[].categoryId` | number |  |
| `videos[].categoryLink` | string |  |
| `videos[].categoryName` | string |  |
| `videos[].createdAt` | string |  |
| `videos[].duration` | string |  |
| `videos[].embedUrl` | string |  |
| `videos[].formValues` | object |  |
| `videos[].formValues.name` | string |  |
| `videos[].id` | number |  |
| `videos[].shareThumbnail` | string |  |
| `videos[].shareUrl` | string |  |
| `videos[].thumbnail` | string |  |
| `videos[].title` | string |  |
| `videos[].token` | string |  |

## Native endpoint

Through the native Hippo Video API, this operation is `GET /api/v1/me/videos/list` (base URL `https://www.hippovideo.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-videos.md) for the provider-specific parameters and requirements.

