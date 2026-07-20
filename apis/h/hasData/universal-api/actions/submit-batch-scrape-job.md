# HasData: Submit Batch Scrape Job

Submits a batch web scrape job to HasData.

```
GET https://connect.mindcloud.co/v1/universal/hasData/latest/actions/submit-batch-scrape-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HasData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasData/latest/actions/submit-batch-scrape-job?connectionId=$CONNECTION_ID&requests%5B%5D.url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requests[].url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasData/latest/actions/submit-batch-scrape-job?${params}`, {
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
| `requests[].aiExtractRules` | object | no | Structured extraction schema for this batch item. |
| `requests[].outputFormat[]` | array<string> | no | Formats to return for this batch item. |
| `requests[].url` | string | yes | Public URL to scrape for this batch item. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string | Created batch job identifier. |
| `status` | string | Batch submission status. |

## Native endpoint

Through the native HasData API, this operation is `POST /scrape/batch/web` (base URL `https://api.hasdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-batch-scrape-job.md) for the provider-specific parameters and requirements.

