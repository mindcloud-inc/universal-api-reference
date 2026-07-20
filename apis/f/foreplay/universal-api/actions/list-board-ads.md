# Foreplay: List Board Ads

Retrieves ads from a specific Foreplay board.

```
GET https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/list-board-ads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Foreplay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/list-board-ads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/list-board-ads?${params}`, {
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
| `boardId` | string | no | Board ID to search for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ad_id": "string",
      "avatar": "string",
      "brand_id": "string",
      "categories": [
        "string"
      ],
      "cta_title": "string",
      "cta_type": "string",
      "description": "string",
      "display_format": "string",
      "headline": "string",
      "id": "string",
      "image": "string",
      "languages": [
        "string"
      ],
      "link_url": "https://example.com",
      "live": true,
      "market_target": "string",
      "name": "Ava Chen",
      "persona": {
        "age": "string",
        "gender": "string"
      },
      "product_category": "string",
      "publisher_platform": [
        "string"
      ],
      "running_duration": {
        "days": 1
      },
      "started_running": 1,
      "thumbnail": "string",
      "type": "string",
      "video": "string",
      "video_duration": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ad_id` | string |  |
| `avatar` | string |  |
| `brand_id` | string |  |
| `categories[]` | string |  |
| `cta_title` | string |  |
| `cta_type` | string |  |
| `description` | string |  |
| `display_format` | string |  |
| `headline` | string |  |
| `id` | string |  |
| `image` | string |  |
| `languages[]` | string |  |
| `link_url` | string |  |
| `live` | boolean |  |
| `market_target` | string |  |
| `name` | string |  |
| `persona.age` | string |  |
| `persona.gender` | string |  |
| `product_category` | string |  |
| `publisher_platform[]` | string |  |
| `running_duration.days` | number |  |
| `started_running` | number |  |
| `thumbnail` | string |  |
| `type` | string |  |
| `video` | string |  |
| `video_duration` | number |  |

## Native endpoint

Through the native Foreplay API, this operation is `GET /api/board/ads` (base URL `https://public.api.foreplay.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-board-ads.md) for the provider-specific parameters and requirements.

