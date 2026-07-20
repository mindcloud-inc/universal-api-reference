# ScrapingDog: Autocomplete Google Trends

Retrieves Google Trends autocomplete suggestions through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/autocomplete-google-trends
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/autocomplete-google-trends?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/autocomplete-google-trends?${params}`, {
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
| `query` | string | yes | Search query for Google Trends autocomplete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "suggestions": {
        "link": "https://example.com",
        "mid": "string",
        "title": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `suggestions` | array<object> |  |
| `suggestions.link` | string |  |
| `suggestions.mid` | string |  |
| `suggestions.title` | string |  |
| `suggestions.type` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_trends/autocomplete` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete-google-trends.md) for the provider-specific parameters and requirements.

