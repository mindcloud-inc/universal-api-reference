# YouTube: Get Video Rating

Retrieves the authenticated user's rating for YouTube videos.

```
GET https://connect.mindcloud.co/v1/universal/youtube/latest/actions/get-video-rating
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouTube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/get-video-rating?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youtube/latest/actions/get-video-rating?${params}`, {
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
| `id` | string | yes | One or more YouTube video IDs. Accepts multiple values in one string, delimited by `,`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `onBehalfOfContentOwner` | string | no | Content owner ID when acting on behalf of a CMS user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rating": "string",
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rating` | string |  |
| `videoId` | string |  |

## Native endpoint

Through the native YouTube API, this operation is `GET /youtube/v3/videos/getRating` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-rating.md) for the provider-specific parameters and requirements.

