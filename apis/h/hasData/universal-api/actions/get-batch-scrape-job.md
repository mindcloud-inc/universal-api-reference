# HasData: Get Batch Scrape Job

Retrieves a batch scrape job from HasData.

```
GET https://connect.mindcloud.co/v1/universal/hasData/latest/actions/get-batch-scrape-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HasData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasData/latest/actions/get-batch-scrape-job?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasData/latest/actions/get-batch-scrape-job?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
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
| `data` | object | Batch job progress details. |
| `jobId` | string | Batch job identifier. |
| `status` | string | Batch job request status. |

## Native endpoint

Through the native HasData API, this operation is `GET /scrape/batch/web/:jobId` (base URL `https://api.hasdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-scrape-job.md) for the provider-specific parameters and requirements.

