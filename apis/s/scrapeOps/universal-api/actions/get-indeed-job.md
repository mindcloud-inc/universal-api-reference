# ScrapeOps: Get Indeed Job

Retrieves Indeed job details from ScrapeOps.

```
GET https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/get-indeed-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeOps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/get-indeed-job?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/get-indeed-job?${params}`, {
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
| `country` | string | no |  |
| `jobId` | string | no | Indeed job ID to fetch. |
| `tld` | string | no |  |
| `url` | string | no | Full Indeed job URL to fetch. |

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
      "description": "string",
      "educations": [
        [
          "string"
        ]
      ],
      "location": "string",
      "salary": {
        "max": 1,
        "min": 1,
        "text": "string",
        "type": "string"
      },
      "skills": [
        [
          "string"
        ]
      ],
      "title": "string"
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
| `description` | string | Job description. |
| `educations[]` | array<string> | Job educations. |
| `location` | string | Job location. |
| `salary.max` | number | Maximum salary. |
| `salary.min` | number | Minimum salary. |
| `salary.text` | string | Salary text. |
| `salary.type` | string | Salary type. |
| `skills[]` | array<string> | Job skills. |
| `title` | string | Job title. |

## Native endpoint

Through the native ScrapeOps API, this operation is `GET https://proxy.scrapeops.io/v1/structured-data/indeed/job-detail` (base URL `http://headers.scrapeops.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-indeed-job.md) for the provider-specific parameters and requirements.

