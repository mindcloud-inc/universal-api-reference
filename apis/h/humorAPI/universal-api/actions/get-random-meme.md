# Humor API: Get Random Meme



```
GET https://connect.mindcloud.co/v1/universal/humorAPI/latest/actions/get-random-meme
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Humor API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/humorAPI/latest/actions/get-random-meme?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/humorAPI/latest/actions/get-random-meme?${params}`, {
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
| `keywords` | string | no | Comma-separated words that must occur in the meme. |
| `keywordsInImage` | boolean | no | Whether keywords must occur in the image. |
| `mediaType` | string | no | Media type, such as image, video, jpg, png, or gif. |
| `minRating` | number | no | Minimum meme rating between 0 and 10. |
| `maxAgeDays` | number | no | Maximum meme age in days. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "height": 1,
      "id": 1,
      "ratio": 1,
      "type": "string",
      "url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `height` | number |  |
| `id` | number |  |
| `ratio` | number |  |
| `type` | string |  |
| `url` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Humor API API, this operation is `GET /memes/random` (base URL `https://api.humorapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-meme.md) for the provider-specific parameters and requirements.

