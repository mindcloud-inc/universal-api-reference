# Botster: Get Job

Retrieves a Botster job and its runs.

```
GET https://connect.mindcloud.co/v1/universal/botster/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botster/latest/actions/get-job?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botster/latest/actions/get-job?${params}`, {
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
| `jobId` | string | yes | The Botster job UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job": {
        "bot": {
          "id": "string",
          "name": "Ava Chen"
        },
        "created_at": 1,
        "finished": true,
        "finished_at": 1,
        "id": "string",
        "name": "Ava Chen",
        "options": {},
        "runs": [
          {}
        ],
        "started_at": 1,
        "state": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job.bot.id` | string | Identifier of the Botster bot that owns the job. |
| `job.bot.name` | string | Display name of the Botster bot that owns the job. |
| `job.created_at` | number | Unix timestamp when the job was created. |
| `job.finished` | boolean | Whether the job has finished processing. |
| `job.finished_at` | number | Unix timestamp when processing finished. |
| `job.id` | string | Unique Botster job identifier. |
| `job.name` | string | Botster job name. |
| `job.options` | object | Bot-specific options captured for the job. |
| `job.runs` | array<object> | Run records associated with the job. |
| `job.started_at` | number | Unix timestamp when processing started. |
| `job.state` | string | Current Botster job state. |

## Native endpoint

Through the native Botster API, this operation is `GET /jobs/:jobId` (base URL `https://botster.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

