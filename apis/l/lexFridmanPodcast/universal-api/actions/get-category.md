# Lex Fridman Podcast: Get Category

Retrieves a category from Lex Fridman Podcast.

```
GET https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/get-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lex Fridman Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/get-category?connectionId=$CONNECTION_ID&id=3392" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "3392"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/get-category?${params}`, {
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
| `id` | string | yes | The category ID. Default: `3392`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "description": "string",
      "id": 1,
      "link": "https://example.com",
      "name": "Ava Chen",
      "parent": 1,
      "slug": "string",
      "taxonomy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `description` | string |  |
| `id` | number |  |
| `link` | string |  |
| `name` | string |  |
| `parent` | number |  |
| `slug` | string |  |
| `taxonomy` | string |  |

## Native endpoint

Through the native Lex Fridman Podcast API, this operation is `GET /wp-json/wp/v2/categories/:id` (base URL `https://lexfridman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-category.md) for the provider-specific parameters and requirements.

