# Giphy: List Trending Clips

Retrieves trending clips from Giphy.

```
GET https://connect.mindcloud.co/v1/universal/giphy/latest/actions/list-trending-clips
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Giphy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giphy/latest/actions/list-trending-clips?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giphy/latest/actions/list-trending-clips?${params}`, {
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
| `rating` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "altText": "string",
      "analytics": {},
      "analyticsResponsePayload": "string",
      "duration": 1,
      "embedUrl": "https://example.com",
      "id": "string",
      "images": {},
      "isLowContrast": true,
      "rating": "string",
      "slug": "string",
      "title": "string",
      "url": "https://example.com",
      "user": {},
      "video": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `altText` | string |  |
| `analytics` | object |  |
| `analyticsResponsePayload` | string |  |
| `duration` | number |  |
| `embedUrl` | string |  |
| `id` | string |  |
| `images` | object |  |
| `isLowContrast` | boolean |  |
| `rating` | string |  |
| `slug` | string |  |
| `title` | string |  |
| `url` | string |  |
| `user` | object |  |
| `video` | object |  |

## Native endpoint

Through the native Giphy API, this operation is `GET /v1/clips/trending` (base URL `https://api.giphy.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-trending-clips.md) for the provider-specific parameters and requirements.

