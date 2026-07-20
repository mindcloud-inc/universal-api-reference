# Databricks: Get Job Run

Retrieves a job run from the Databricks workspace.

```
GET https://connect.mindcloud.co/v1/universal/databricks/latest/actions/get-job-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/get-job-run?connectionId=$CONNECTION_ID&runId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/databricks/latest/actions/get-job-run?${params}`, {
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
| `runId` | number | yes | The canonical identifier of the run for which to retrieve the metadata. This field is required. |
| `includeHistory` | boolean | no | Whether to include the repair history in the response. |
| `includeResolvedValues` | boolean | no | Whether to include resolved parameter values in the response. |
| `pageToken` | string | no | Use `next_page_token` returned from the previous GetRun response to request the next page of the run's array properties. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attempt_number": 1,
      "cleanup_duration": 1,
      "cluster_instance": {},
      "cluster_spec": {},
      "creator_user_name": "Ava Chen",
      "description": "string",
      "effective_performance_target": "string",
      "end_time": 1,
      "execution_duration": 1,
      "git_source": {},
      "has_more": true,
      "job_clusters": [
        {}
      ],
      "job_id": 1,
      "job_parameters": [
        {}
      ],
      "job_run_id": 1,
      "next_page_token": "string",
      "number_in_job": 1,
      "original_attempt_run_id": 1,
      "overriding_parameters": {},
      "queue_duration": 1,
      "repair_history": [
        {}
      ],
      "run_duration": 1,
      "run_id": 1,
      "run_name": "Ava Chen",
      "run_page_url": "https://example.com",
      "run_type": "string",
      "schedule": {},
      "setup_duration": 1,
      "start_time": 1,
      "state": {},
      "status": {},
      "tasks": [
        {}
      ],
      "trigger": "string",
      "trigger_info": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attempt_number` | number |  |
| `cleanup_duration` | number |  |
| `cluster_instance` | object |  |
| `cluster_spec` | object |  |
| `creator_user_name` | string |  |
| `description` | string |  |
| `effective_performance_target` | string |  |
| `end_time` | number |  |
| `execution_duration` | number |  |
| `git_source` | object |  |
| `has_more` | boolean |  |
| `job_clusters` | array<object> |  |
| `job_id` | number |  |
| `job_parameters` | array<object> |  |
| `job_run_id` | number |  |
| `next_page_token` | string |  |
| `number_in_job` | number |  |
| `original_attempt_run_id` | number |  |
| `overriding_parameters` | object |  |
| `queue_duration` | number |  |
| `repair_history` | array<object> |  |
| `run_duration` | number |  |
| `run_id` | number |  |
| `run_name` | string |  |
| `run_page_url` | string |  |
| `run_type` | string |  |
| `schedule` | object |  |
| `setup_duration` | number |  |
| `start_time` | number |  |
| `state` | object |  |
| `status` | object |  |
| `tasks` | array<object> |  |
| `trigger` | string |  |
| `trigger_info` | object |  |

## Native endpoint

Through the native Databricks API, this operation is `GET {{credentials.host}}/api/2.2/jobs/runs/get` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-run.md) for the provider-specific parameters and requirements.

