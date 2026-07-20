# Run Job Now with Databricks

Runs a Databricks job immediately by job ID.

## Endpoint

- **Method:** `POST`
- **Path:** `{host}/api/2.2/jobs/run-now`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Run Job Now](https://docs.databricks.com/api/workspace/jobs/runnow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idempotency_token` | body | `string` | no | An optional token to guarantee the idempotency of job run requests. If a run with the provided token already exists, the request does not create a new run but returns the ID of the existing run instead. If a run with the provided token is deleted, an error is returned.  If you specify the idempotency token, upon failure you can retry until the request succeeds. Databricks guarantees that exactly one run is launched with that idempotency token.  This token must have at most 64 characters.  For more information, see [How to ensure idempotency for jobs](https://kb.databricks.com/jobs/jobs-idempotency.html). |
| `job_id` | body | `number` | yes | The ID of the job to be executed |
| `job_parameters` | body | `object` | no | Job-level parameters used in the run. for example `"param": "overriding_val"` |
| `only` | body | `list<string>` | yes | A list of task keys to run inside of the job. If this field is not provided, all tasks in the job will be run. |
| `performance_target` | body | `string` | no | PerformanceTarget defines how performant (lower latency) or cost efficient the execution of run on serverless compute should be. The performance mode on the job or pipeline should map to a performance setting that is passed to Cluster Manager (see cluster-common PerformanceTarget). |
| `pipeline_params` | body | `object` | no | — |
| `full_refresh` | body | `boolean` | no | If true, triggers a full refresh on the delta live table. |
| `queue` | body | `object` | no | — |
| `queue.enabled` | body | `boolean` | yes | If true, enable queueing for the job. This is a required field. |
