# Vimeo: List Video Tags

Retrieves tags for a Vimeo video.

```
GET https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-video-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vimeo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-video-tags?connectionId=$CONNECTION_ID&limit=25&offset=0&videoId=1077404152" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "videoId": "1077404152"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-video-tags?${params}`, {
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
| `videoId` | number | yes | The ID of the video. Example: `1077404152`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canonical": "string",
      "metadata": {},
      "name": "Ava Chen",
      "resourceKey": "string",
      "tag": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canonical` | string | Canonical tag slug. |
| `metadata` | object | Tag metadata. |
| `name` | string | Tag display name. |
| `resourceKey` | string | Tag resource key. |
| `tag` | string | Tag label. |
| `uri` | string | Tag URI. |

## Native endpoint

Through the native Vimeo API, this operation is `GET /videos/:video_id/tags` (base URL `https://api.vimeo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-video-tags.md) for the provider-specific parameters and requirements.

