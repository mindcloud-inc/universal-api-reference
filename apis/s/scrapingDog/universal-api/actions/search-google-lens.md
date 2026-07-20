# ScrapingDog: Search Google Lens

Retrieves Google Lens results through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-lens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-lens?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-lens?${params}`, {
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
| `url` | string | yes | Google Lens URL, typically a lens.google.com upload-by-url link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lens_results": {
        "link": "https://example.com",
        "position": 1,
        "source": "string",
        "source_favicon": "string",
        "thumbnail": "string",
        "title": "string"
      },
      "related_searches": {
        "link": "https://example.com",
        "thumbnail": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lens_results` | array<object> |  |
| `lens_results.link` | string |  |
| `lens_results.position` | number |  |
| `lens_results.source` | string |  |
| `lens_results.source_favicon` | string |  |
| `lens_results.thumbnail` | string |  |
| `lens_results.title` | string |  |
| `related_searches` | array<object> |  |
| `related_searches.link` | string |  |
| `related_searches.thumbnail` | string |  |
| `related_searches.title` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_lens` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-lens.md) for the provider-specific parameters and requirements.

