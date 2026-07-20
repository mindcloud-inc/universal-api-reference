# ActivityInfo: Get Job Status

Retrieves a job's status from ActivityInfo.

```
GET https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivityInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-job-status?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-job-status?${params}`, {
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
| `jobId` | string | yes | ActivityInfo long-running job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "descriptor": {},
      "error": {},
      "id": "string",
      "jobResult": {},
      "percentComplete": 1,
      "state": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `descriptor` | object | Job descriptor. |
| `error` | object | Failure reason, when failed. |
| `id` | string | Job ID. |
| `jobResult` | object | Job result. |
| `percentComplete` | number | Completion percentage. |
| `state` | string | Job state. |
| `userId` | string | User that started the job. |

## Native endpoint

Through the native ActivityInfo API, this operation is `GET /resources/jobs/:jobId` (base URL `https://www.activityinfo.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-status.md) for the provider-specific parameters and requirements.

