# ScrapeOps: Search Indeed Companies

Retrieves Indeed company search results from ScrapeOps.

```
GET https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/search-indeed-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeOps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/search-indeed-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/search-indeed-companies?${params}`, {
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
| `location` | string | no | Location for the Indeed company search. |
| `query` | string | no | Indeed company search query. |
| `url` | string | no | Full Indeed companies search URL to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "industries": [
        [
          "string"
        ]
      ],
      "jobs_url": "https://example.com",
      "name": "Ava Chen",
      "overview_url": "https://example.com",
      "rating": 1,
      "review_count": 1,
      "reviews_url": "https://example.com",
      "salaries_url": "https://example.com",
      "thumbnail": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Company description. |
| `industries[]` | array<string> | Company industries. |
| `jobs_url` | string | Company jobs URL. |
| `name` | string | Company name. |
| `overview_url` | string | Company overview URL. |
| `rating` | number | Company rating. |
| `review_count` | number | Review count. |
| `reviews_url` | string | Reviews URL. |
| `salaries_url` | string | Salaries URL. |
| `thumbnail` | string | Company thumbnail URL. |

## Native endpoint

Through the native ScrapeOps API, this operation is `GET https://proxy.scrapeops.io/v1/structured-data/indeed/company-search` (base URL `http://headers.scrapeops.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-indeed-companies.md) for the provider-specific parameters and requirements.

