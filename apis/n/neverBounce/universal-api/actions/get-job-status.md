# NeverBounce: Get Job Status

Retrieves the current status of a NeverBounce job.

```
GET https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/get-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeverBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/get-job-status?connectionId=$CONNECTION_ID&jobId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/get-job-status?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounceEstimate": 1,
      "createdAt": "string",
      "executionTime": 1,
      "failureReason": "string",
      "filename": "Ava Chen",
      "finishedAt": "string",
      "id": 1,
      "jobStatus": "string",
      "percentComplete": 1,
      "startedAt": "string",
      "status": "string",
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounceEstimate` | number |  |
| `createdAt` | string |  |
| `executionTime` | number |  |
| `failureReason` | string |  |
| `filename` | string |  |
| `finishedAt` | string |  |
| `id` | number |  |
| `jobStatus` | string |  |
| `percentComplete` | number |  |
| `startedAt` | string |  |
| `status` | string |  |
| `total` | object |  |
| `total.badSyntax` | number |  |
| `total.billable` | number |  |
| `total.catchall` | number |  |
| `total.disposable` | number |  |
| `total.duplicates` | number |  |
| `total.invalid` | number |  |
| `total.processed` | number |  |
| `total.records` | number |  |
| `total.unknown` | number |  |
| `total.valid` | number |  |

## Native endpoint

Through the native NeverBounce API, this operation is `GET /jobs/status` (base URL `https://api.neverbounce.com/v4.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-status.md) for the provider-specific parameters and requirements.

