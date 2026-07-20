# Datastreamer: Create Job

Creates a new job in Datastreamer.

```
POST https://connect.mindcloud.co/v1/universal/datastreamer/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datastreamer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datastreamer/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pipelineId": "string",
  "componentId": "string",
  "job_name": "Ava Chen",
  "data_source": "string",
  "query": {},
  "job_type": "periodic",
  "schedule": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datastreamer/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pipelineId": "string",
    "componentId": "string",
    "job_name": "Ava Chen",
    "data_source": "string",
    "query": {},
    "job_type": "periodic",
    "schedule": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pipelineId` | string | yes |  |
| `componentId` | string | yes |  |
| `ready` | boolean | no | Default: `true`. |
| `job_name` | string | yes | Job name to persist on the created job. |
| `data_source` | string | yes | Datastreamer data source for the job. |
| `query` | object | yes | Full query object for the created job payload. |
| `job_type` | string | yes | Job type, for example periodic. Default: `periodic`. |
| `schedule` | string | yes | Cron schedule for a periodic job. |
| `label` | string | no | Optional label applied to job output. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Datastreamer API returns.

## Native endpoint

Through the native Datastreamer API, this operation is `POST /api/pipelines/:pipelineId/components/:componentId/jobs` (base URL `https://api.platform.datastreamer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

