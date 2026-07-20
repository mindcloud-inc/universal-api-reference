# ScrapingDog: Search Google Jobs

Retrieves Google Jobs search results through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-jobs?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-jobs?${params}`, {
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
| `query` | string | yes | Search query for Google Jobs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobs_results": {
        "apply_links": {
          "link": "https://example.com",
          "title": "https://example.com"
        },
        "company_name": "Ava Chen",
        "description": "string",
        "extensions": [
          "string"
        ],
        "location": "string",
        "title": "string",
        "url": "https://example.com",
        "via": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobs_results` | array<object> |  |
| `jobs_results.apply_links` | array<object> |  |
| `jobs_results.apply_links.link` | string |  |
| `jobs_results.apply_links.title` | string |  |
| `jobs_results.company_name` | string |  |
| `jobs_results.description` | string |  |
| `jobs_results.extensions` | array<string> |  |
| `jobs_results.location` | string |  |
| `jobs_results.title` | string |  |
| `jobs_results.url` | string |  |
| `jobs_results.via` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_jobs` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-jobs.md) for the provider-specific parameters and requirements.

