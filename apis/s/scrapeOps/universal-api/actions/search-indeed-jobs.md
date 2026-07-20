# ScrapeOps: Search Indeed Jobs

Retrieves Indeed job search results from ScrapeOps.

```
GET https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/search-indeed-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeOps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/search-indeed-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/search-indeed-jobs?${params}`, {
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
| `location` | string | no | Location for the Indeed job search. |
| `query` | string | no | Indeed job search query. |
| `url` | string | no | Full Indeed jobs search URL to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {
        "name": "Ava Chen",
        "overview_url": "https://example.com",
        "rating": 1,
        "review_count": 1
      },
      "create_date": "string",
      "is_expired": true,
      "is_new_job": true,
      "is_urgently_hiring": true,
      "location": "string",
      "salary": {
        "max": 1,
        "min": 1,
        "text": "string",
        "type": "string"
      },
      "snippet": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company.name` | string | Company name. |
| `company.overview_url` | string | Company overview URL. |
| `company.rating` | number | Company rating. |
| `company.review_count` | number | Company review count. |
| `create_date` | string | Job creation date. |
| `is_expired` | boolean | Whether the job is expired. |
| `is_new_job` | boolean | Whether the job is marked new. |
| `is_urgently_hiring` | boolean | Whether the job is urgently hiring. |
| `location` | string | Job location. |
| `salary.max` | number | Maximum salary. |
| `salary.min` | number | Minimum salary. |
| `salary.text` | string | Salary text. |
| `salary.type` | string | Salary type. |
| `snippet` | string | Job snippet. |
| `title` | string | Job title. |
| `url` | string | Indeed job URL. |

## Native endpoint

Through the native ScrapeOps API, this operation is `GET https://proxy.scrapeops.io/v1/structured-data/indeed/job-search` (base URL `http://headers.scrapeops.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-indeed-jobs.md) for the provider-specific parameters and requirements.

