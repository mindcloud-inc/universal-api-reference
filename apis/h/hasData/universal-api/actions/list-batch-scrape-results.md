# HasData: List Batch Scrape Results

Retrieves results for a HasData batch scrape job.

```
GET https://connect.mindcloud.co/v1/universal/hasData/latest/actions/list-batch-scrape-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HasData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasData/latest/actions/list-batch-scrape-results?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasData/latest/actions/list-batch-scrape-results?${params}`, {
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
| `jobId` | string | yes | Batch scrape job ID. |
| `limit` | number | no | Maximum number of results per page. |
| `page` | number | no | Result page number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "limit": 1,
      "page": 1,
      "results": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limit` | number | Requested page size. |
| `page` | number | Current results page. |
| `results` | array<object> | Batch result rows. |
| `total` | number | Total available batch results. |

## Native endpoint

Through the native HasData API, this operation is `GET /scrape/batch/web/:jobId/results` (base URL `https://api.hasdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-batch-scrape-results.md) for the provider-specific parameters and requirements.

