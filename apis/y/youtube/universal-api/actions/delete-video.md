# YouTube: Delete Video

Deletes an existing video from YouTube.

```
DELETE https://connect.mindcloud.co/v1/universal/youtube/latest/actions/delete-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouTube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/delete-video?connectionId=$CONNECTION_ID&id=dQw4w9WgXcQ" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "dQw4w9WgXcQ"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youtube/latest/actions/delete-video?${params}`, {
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
| `id` | string | yes | Example: `dQw4w9WgXcQ`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `onBehalfOfContentOwner` | string | no |  |

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
| `value` | string | The raw response body. Official YouTube Data API docs state this method returns HTTP 204 No Content on success. Source: https://developers.google.com/youtube/v3/docs/videos/delete |

## Native endpoint

Through the native YouTube API, this operation is `DELETE /youtube/v3/videos` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-video.md) for the provider-specific parameters and requirements.

