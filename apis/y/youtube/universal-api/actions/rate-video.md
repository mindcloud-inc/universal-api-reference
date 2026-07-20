# YouTube: Rate Video

Sets the authenticated user's rating for a YouTube video.

```
PUT https://connect.mindcloud.co/v1/universal/youtube/latest/actions/rate-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouTube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/rate-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "rating": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/youtube/latest/actions/rate-video', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "rating": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | YouTube video ID. |
| `rating` | string | yes | Rating to set for the video. |

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
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | The raw response body. Official YouTube Data API docs state this method returns HTTP 204 No Content on success. Source: https://developers.google.com/youtube/v3/docs/videos/rate |

## Native endpoint

Through the native YouTube API, this operation is `POST /youtube/v3/videos/rate` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rate-video.md) for the provider-specific parameters and requirements.

