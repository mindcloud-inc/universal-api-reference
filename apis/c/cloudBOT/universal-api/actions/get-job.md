# Cloud BOT: Get Job

Retrieves a job from Cloud BOT.

```
GET https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud BOT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/get-job?connectionId=$CONNECTION_ID&publicId=string&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publicId": "string",
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/get-job?${params}`, {
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
| `publicId` | string | yes | Public ID of API |
| `jobId` | string | yes | JOB ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "botId": "string",
      "botName": "Ava Chen",
      "code": 1,
      "elapsedTime": 1,
      "jobId": "string",
      "output": {},
      "startTime": "2026-05-07T12:00:00.000Z",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botId` | string | BOT ID |
| `botName` | string | BOT name |
| `code` | number | Response status code |
| `elapsedTime` | number | Elapsed time in seconds |
| `jobId` | string | JOB ID |
| `output` | object | BOT output object |
| `startTime` | date | Job start time |
| `status` | number | Job status code |

## Native endpoint

Through the native Cloud BOT API, this operation is `GET /:public_id/jobs/:job_id` (base URL `https://api.c-bot.pro`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

