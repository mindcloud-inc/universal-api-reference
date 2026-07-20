# ScrapingDog: Search Google

Retrieves Google search results through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google?${params}`, {
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
| `query` | string | yes | Search query to run on Google. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ads": [
        "string"
      ],
      "organic_data": {
        "displayed_link": "https://example.com",
        "extended_sitelinks": {
          "link": "https://example.com",
          "title": "https://example.com"
        },
        "link": "https://example.com",
        "rank": 1,
        "snippet": "string",
        "title": "string"
      },
      "people_also_ask": {
        "answers": "string",
        "id": "string",
        "question": "string",
        "rank": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ads` | array<string> |  |
| `organic_data` | array<object> |  |
| `organic_data.displayed_link` | string |  |
| `organic_data.extended_sitelinks` | array<object> |  |
| `organic_data.extended_sitelinks.link` | string |  |
| `organic_data.extended_sitelinks.title` | string |  |
| `organic_data.link` | string |  |
| `organic_data.rank` | number |  |
| `organic_data.snippet` | string |  |
| `organic_data.title` | string |  |
| `people_also_ask` | array<object> |  |
| `people_also_ask.answers` | string |  |
| `people_also_ask.id` | string |  |
| `people_also_ask.question` | string |  |
| `people_also_ask.rank` | number |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google.md) for the provider-specific parameters and requirements.

