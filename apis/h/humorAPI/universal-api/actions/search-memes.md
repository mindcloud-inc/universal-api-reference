# Humor API: Search Memes



```
GET https://connect.mindcloud.co/v1/universal/humorAPI/latest/actions/search-memes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Humor API `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/humorAPI/latest/actions/search-memes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/humorAPI/latest/actions/search-memes?${params}`, {
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
      "available": 1,
      "memes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | number |  |
| `memes` | array<object> |  |

## Native endpoint

Through the native Humor API API, this operation is `GET /memes/search` (base URL `https://api.humorapi.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-memes.md) for the provider-specific parameters and requirements.

