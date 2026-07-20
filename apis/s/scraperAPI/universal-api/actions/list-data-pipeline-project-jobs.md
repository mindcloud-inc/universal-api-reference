# ScraperAPI: List DataPipeline Project Jobs

Retrieves DataPipeline project jobs from ScraperAPI.

```
GET https://connect.mindcloud.co/v1/universal/scraperAPI/latest/actions/list-data-pipeline-project-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScraperAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scraperAPI/latest/actions/list-data-pipeline-project-jobs?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scraperAPI/latest/actions/list-data-pipeline-project-jobs?${params}`, {
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
| `id` | number | yes | The DataPipeline project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attempts": 1,
      "id": "string",
      "meta": {},
      "response": {},
      "status": "string",
      "statusUrl": "https://example.com",
      "supposedToRunAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attempts` | number |  |
| `id` | string |  |
| `meta` | object |  |
| `response` | object |  |
| `status` | string |  |
| `statusUrl` | string |  |
| `supposedToRunAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native ScraperAPI API, this operation is `GET https://datapipeline.scraperapi.com/api/projects/:id/jobs` (base URL `https://api.scraperapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-data-pipeline-project-jobs.md) for the provider-specific parameters and requirements.

