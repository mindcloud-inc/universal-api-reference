# Verify550: Get Verification Job

Retrieves a verification job from Verify550.

```
GET https://connect.mindcloud.co/v1/universal/verify550/latest/actions/get-verification-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verify550 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verify550/latest/actions/get-verification-job?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verify550/latest/actions/get-verification-job?${params}`, {
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
| `jobId` | string | yes | Verify550 bulk verification job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "completionTime": "2026-05-07T12:00:00.000Z",
        "count": 1,
        "duplicates": 1,
        "file_name": "Ava Chen",
        "jobId": "string",
        "processed": 1,
        "startTime": "2026-05-07T12:00:00.000Z",
        "status": "string",
        "suppression_results": {},
        "uploadTime": "2026-05-07T12:00:00.000Z"
      },
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.completionTime` | date |  |
| `data.count` | number |  |
| `data.duplicates` | number |  |
| `data.file_name` | string |  |
| `data.jobId` | string |  |
| `data.processed` | number |  |
| `data.startTime` | date |  |
| `data.status` | string |  |
| `data.suppression_results` | object |  |
| `data.uploadTime` | date |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Verify550 API, this operation is `GET /getjob/:jobId` (base URL `https://app.verify550.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-verification-job.md) for the provider-specific parameters and requirements.

