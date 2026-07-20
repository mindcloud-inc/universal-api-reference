# ScrapingDog: Search Google Images

Retrieves Google Images search results through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-images?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-images?${params}`, {
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
| `query` | string | yes | Search query for Google Images. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ads": [
        "string"
      ],
      "images_results": {
        "image": "string",
        "is_product": true,
        "know_more_link": "https://example.com",
        "link": "https://example.com",
        "original": "string",
        "original_height": 1,
        "original_size": "string",
        "original_width": 1,
        "rank": 1,
        "source": "string",
        "title": "string"
      },
      "time_taken": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ads` | array<string> |  |
| `images_results` | array<object> |  |
| `images_results.image` | string |  |
| `images_results.is_product` | boolean |  |
| `images_results.know_more_link` | string |  |
| `images_results.link` | string |  |
| `images_results.original` | string |  |
| `images_results.original_height` | number |  |
| `images_results.original_size` | string |  |
| `images_results.original_width` | number |  |
| `images_results.rank` | number |  |
| `images_results.source` | string |  |
| `images_results.title` | string |  |
| `time_taken` | number |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_images` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-images.md) for the provider-specific parameters and requirements.

