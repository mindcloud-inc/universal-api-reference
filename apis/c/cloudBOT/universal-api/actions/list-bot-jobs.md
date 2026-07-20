# Cloud BOT: List Bot Jobs

Retrieves bot jobs from Cloud BOT.

```
GET https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/list-bot-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud BOT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/list-bot-jobs?connectionId=$CONNECTION_ID&publicId=string&botId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publicId": "string",
  "botId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/list-bot-jobs?${params}`, {
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
| `botId` | string | yes | BOT ID |
| `limit` | number | no | Maximum number of jobs to return |
| `sortOrder` | string | no | Sort order asc or desc |
| `statuses` | string | no | Comma-separated job statuses: 0 succeeded, 1 error, 2 executing |
| `datetimeFrom` | string | no | Return jobs created after this ISO 8601 timestamp |
| `datetimeTo` | string | no | Return jobs created before this ISO 8601 timestamp |
| `idFrom` | string | no | Return jobs with IDs greater than this value |
| `idTo` | string | no | Return jobs with IDs smaller than this value |
| `properties` | string | no | Comma-separated extra job fields |

## Response

```json
{
  "success": true,
  "data": [
    {
      "botId": "string",
      "botName": "Ava Chen",
      "castUrl": "https://example.com",
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
| `castUrl` | string | Cast URL for executing jobs |
| `code` | number | Response status code |
| `elapsedTime` | number | Elapsed time in seconds |
| `jobId` | string | JOB ID |
| `output` | object | BOT output object when requested or completed |
| `startTime` | date | Job start time |
| `status` | number | Job status code |

## Native endpoint

Through the native Cloud BOT API, this operation is `GET /:public_id/bots/:bot_id/jobs` (base URL `https://api.c-bot.pro`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bot-jobs.md) for the provider-specific parameters and requirements.

