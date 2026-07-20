# List Job Runs with Databricks

Retrieves job runs from the Databricks workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `{host}/api/2.2/jobs/runs/list`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [List Job Runs](https://docs.databricks.com/api/workspace/jobs/listruns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | query | `number` | no | The job for which to list runs. If omitted, the Jobs service lists runs from all jobs. |
| `active_only` | query | `boolean` | no | If active_only is `true`, only active runs are included in the results; otherwise, lists both active and completed runs. An active run is a run in the `QUEUED`, `PENDING`, `RUNNING`, or `TERMINATING`. This field cannot be `true` when completed_only is `true`. |
| `completed_only` | query | `boolean` | no | If completed_only is `true`, only completed runs are included in the results; otherwise, lists both active and completed runs. This field cannot be `true` when active_only is `true`. |
| `limit` | query | `number` | no | The number of runs to return. This value must be greater than 0 and less than 25. The default value is 20. If a request specifies a limit of 0, the service instead uses the maximum limit. |
| `run_type` | query | `string` | no | The type of runs to return. For a description of run types, see :method:jobs/getRun. |
| `expand_tasks` | query | `boolean` | no | Whether to include task and cluster details in the response. Note that only the first 100 elements will be shown. Use :method:jobs/getrun to paginate through all tasks and clusters. |
| `start_time_from` | query | `number` | no | Show runs that started _at or after_ this value. The value must be a UTC timestamp in milliseconds. Can be combined with _start_time_to_ to filter by a time range. |
| `start_time_to` | query | `number` | no | Show runs that started _at or before_ this value. The value must be a UTC timestamp in milliseconds. Can be combined with _start_time_from_ to filter by a time range. |
| `page_token` | query | `string` | no | Use `next_page_token` or `prev_page_token` returned from the previous request to list the next or previous page of runs respectively. |
