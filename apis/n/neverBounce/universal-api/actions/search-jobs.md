# NeverBounce: Search Jobs

Finds NeverBounce jobs by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/search-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeverBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/search-jobs?connectionId=$CONNECTION_ID&jobId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/search-jobs?${params}`, {
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
| `jobId` | number | yes | NeverBounce job identifier. |
| `page` | number | no | Result page to retrieve. |
| `itemsPerPage` | number | no | Number of jobs to return per page. |
| `filename` | string | no | Filter jobs by filename. |
| `jobStatus` | string | no | Filter jobs by NeverBounce job status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "executionTime": 1,
      "query": {
        "itemsPerPage": 1,
        "jobId": 1,
        "page": 1
      },
      "results": [
        {
          "bounceEstimate": 1,
          "createdAt": "string",
          "filename": "Ava Chen",
          "finishedAt": "string",
          "id": 1,
          "jobStatus": "string",
          "percentComplete": 1,
          "startedAt": "string",
          "total": {
            "badSyntax": 1,
            "billable": 1,
            "catchall": 1,
            "disposable": 1,
            "duplicates": 1,
            "invalid": 1,
            "processed": 1,
            "records": 1,
            "unknown": 1,
            "valid": 1
          }
        }
      ],
      "status": "string",
      "totalPages": 1,
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `executionTime` | number |  |
| `query` | object |  |
| `query.itemsPerPage` | number |  |
| `query.jobId` | number |  |
| `query.page` | number |  |
| `results` | array<object> |  |
| `results[].bounceEstimate` | number |  |
| `results[].createdAt` | string |  |
| `results[].filename` | string |  |
| `results[].finishedAt` | string |  |
| `results[].id` | number |  |
| `results[].jobStatus` | string |  |
| `results[].percentComplete` | number |  |
| `results[].startedAt` | string |  |
| `results[].total` | object |  |
| `results[].total.badSyntax` | number |  |
| `results[].total.billable` | number |  |
| `results[].total.catchall` | number |  |
| `results[].total.disposable` | number |  |
| `results[].total.duplicates` | number |  |
| `results[].total.invalid` | number |  |
| `results[].total.processed` | number |  |
| `results[].total.records` | number |  |
| `results[].total.unknown` | number |  |
| `results[].total.valid` | number |  |
| `status` | string |  |
| `totalPages` | number |  |
| `totalResults` | number |  |

## Native endpoint

Through the native NeverBounce API, this operation is `GET /jobs/search` (base URL `https://api.neverbounce.com/v4.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-jobs.md) for the provider-specific parameters and requirements.

