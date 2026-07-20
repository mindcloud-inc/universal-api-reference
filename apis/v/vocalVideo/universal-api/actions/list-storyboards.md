# Vocal Video: List Storyboards

Retrieves storyboard samples from Vocal Video.

```
GET https://connect.mindcloud.co/v1/universal/vocalVideo/latest/actions/list-storyboards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vocal Video `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vocalVideo/latest/actions/list-storyboards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vocalVideo/latest/actions/list-storyboards?${params}`, {
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
      "app_url": "https://example.com",
      "creator": {},
      "description": "string",
      "height": 1,
      "id": 1,
      "internal_title": "string",
      "public_url": "https://example.com",
      "published_at": "2026-05-07T12:00:00.000Z",
      "render_count": 1,
      "replies": [
        {}
      ],
      "slug": "string",
      "title": "string",
      "video_original": {},
      "visibility": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app_url` | string | Storyboard app URL. |
| `creator` | object | Creator metadata. |
| `description` | string | Storyboard description. |
| `height` | number | Rendered height. |
| `id` | number | Storyboard id. |
| `internal_title` | string | Internal storyboard title. |
| `public_url` | string | Published public URL. |
| `published_at` | date | Publish timestamp. |
| `render_count` | number | Render count. |
| `replies` | array<object> | Replies included in the storyboard. |
| `slug` | string | Storyboard slug. |
| `title` | string | Public title. |
| `video_original` | object | Original video metadata. |
| `visibility` | string | Visibility setting. |
| `width` | number | Rendered width. |

## Native endpoint

Through the native Vocal Video API, this operation is `GET /storyboards` (base URL `https://vocalvideo.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-storyboards.md) for the provider-specific parameters and requirements.

