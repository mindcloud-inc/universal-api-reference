# Vimeo: Search Videos

Finds videos in Vimeo by search query.

```
GET https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/search-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vimeo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/search-videos?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/search-videos?${params}`, {
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
| `query` | string | no | The search query. Example: `staff picks`. |
| `filter` | list | no | The attribute by which to filter the results. One of: `CC`, `CC-BY`, `CC-BY-NC`, `CC-BY-NC-ND`, `CC-BY-NC-SA`, `CC-BY-ND`, `CC-BY-SA`, `CC0`, `categories`, `duration`, `in-progress`, `minimum_likes`, `trending`, `upload_date`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `links` | string | no | A comma-separated list of video URLs to find. Example: `https://vimeo.com/122375452,https://vimeo.com/273576296`. |
| `uris` | string | no | A comma-separated list of video URIs to find. Example: `/videos/122375452,/videos/273576296`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "duration": 1,
      "link": "https://example.com",
      "name": "Ava Chen",
      "pictures": {},
      "privacy": {},
      "status": "string",
      "tags": [
        {}
      ],
      "uri": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | date | Video creation time. |
| `description` | string | Video description. |
| `duration` | number | Video duration in seconds. |
| `link` | string | Video link. |
| `name` | string | Video title. |
| `pictures` | object | Video pictures. |
| `privacy` | object | Video privacy settings. |
| `status` | string | Video status. |
| `tags` | array<object> | Video tags. |
| `uri` | string | Video URI. |
| `user` | object | Video owner. |

## Native endpoint

Through the native Vimeo API, this operation is `GET /videos` (base URL `https://api.vimeo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-videos.md) for the provider-specific parameters and requirements.

