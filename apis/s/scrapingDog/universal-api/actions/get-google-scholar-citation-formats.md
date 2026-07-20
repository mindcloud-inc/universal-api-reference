# ScrapingDog: Get Google Scholar Citation Formats

Retrieves Google Scholar citation formats through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-scholar-citation-formats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-scholar-citation-formats?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-scholar-citation-formats?${params}`, {
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
| `query` | string | yes | Citation identifier or query token to retrieve Google Scholar citation formats. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "citations": {
        "snippet": "string",
        "title": "string"
      },
      "links": {
        "link": "https://example.com",
        "name": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `citations` | array<object> |  |
| `citations.snippet` | string |  |
| `citations.title` | string |  |
| `links` | array<object> |  |
| `links.link` | string |  |
| `links.name` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_scholar/cite` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-google-scholar-citation-formats.md) for the provider-specific parameters and requirements.

