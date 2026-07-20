# Databricks: Run Job Now

Runs a Databricks job immediately by job ID.

```
POST https://connect.mindcloud.co/v1/universal/databricks/latest/actions/run-job-now
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/run-job-now" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": 1,
  "only": "string",
  "queue.enabled": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/databricks/latest/actions/run-job-now', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": 1,
    "only": "string",
    "queue.enabled": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idempotencyToken` | string | no | An optional token to guarantee the idempotency of job run requests. If a run with the provided token already exists, the request does not create a new run but returns the ID of the existing run instead. If a run with the provided token is deleted, an error is returned. If you specify the idempotency token, upon failure you can retry until the request succeeds. Databricks guarantees that exactly one run is launched with that idempotency token. This token must have at most 64 characters. For more information, see [How to ensure idempotency for jobs](https://kb.databricks.com/jobs/jobs-idempotency.html). |
| `jobId` | number | yes | The ID of the job to be executed |
| `jobParameters` | object | no | Job-level parameters used in the run. for example `"param": "overriding_val"` |
| `only` | list<string> | yes | A list of task keys to run inside of the job. If this field is not provided, all tasks in the job will be run. |
| `performanceTarget` | string | no | PerformanceTarget defines how performant (lower latency) or cost efficient the execution of run on serverless compute should be. The performance mode on the job or pipeline should map to a performance setting that is passed to Cluster Manager (see cluster-common PerformanceTarget). |
| `pipelineParams` | object | no |  |
| `pipelineParams.fullRefresh` | boolean | no | If true, triggers a full refresh on the delta live table. |
| `queue` | object | no |  |
| `queue.enabled` | boolean | yes | If true, enable queueing for the job. This is a required field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "number_in_job": 1,
      "run_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `number_in_job` | number | A unique identifier for this job run. This is set to the same value as `run_id`. |
| `run_id` | number | The globally unique ID of the newly triggered run. |

## Native endpoint

Through the native Databricks API, this operation is `POST {{credentials.host}}/api/2.2/jobs/run-now` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-job-now.md) for the provider-specific parameters and requirements.

