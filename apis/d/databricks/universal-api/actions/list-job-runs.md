# Databricks: List Job Runs

Retrieves job runs from the Databricks workspace.

```
GET https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-job-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-job-runs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-job-runs?${params}`, {
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
| `jobId` | number | no | The job for which to list runs. If omitted, the Jobs service lists runs from all jobs. |
| `activeOnly` | boolean | no | If active_only is `true`, only active runs are included in the results; otherwise, lists both active and completed runs. An active run is a run in the `QUEUED`, `PENDING`, `RUNNING`, or `TERMINATING`. This field cannot be `true` when completed_only is `true`. |
| `completedOnly` | boolean | no | If completed_only is `true`, only completed runs are included in the results; otherwise, lists both active and completed runs. This field cannot be `true` when active_only is `true`. |
| `limit` | number | no | The number of runs to return. This value must be greater than 0 and less than 25. The default value is 20. If a request specifies a limit of 0, the service instead uses the maximum limit. |
| `runType` | string | no | The type of runs to return. For a description of run types, see :method:jobs/getRun. |
| `expandTasks` | boolean | no | Whether to include task and cluster details in the response. Note that only the first 100 elements will be shown. Use :method:jobs/getrun to paginate through all tasks and clusters. |
| `startTimeFrom` | number | no | Show runs that started _at or after_ this value. The value must be a UTC timestamp in milliseconds. Can be combined with _start_time_to_ to filter by a time range. |
| `startTimeTo` | number | no | Show runs that started _at or before_ this value. The value must be a UTC timestamp in milliseconds. Can be combined with _start_time_from_ to filter by a time range. |
| `pageToken` | string | no | Use `next_page_token` or `prev_page_token` returned from the previous request to list the next or previous page of runs respectively. |

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

Through the native Databricks API, this operation is `GET {{credentials.host}}/api/2.2/jobs/runs/list` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-job-runs.md) for the provider-specific parameters and requirements.

