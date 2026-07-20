# Databricks: Update Job

Updates an existing job in the Databricks workspace.

```
PUT https://connect.mindcloud.co/v1/universal/databricks/latest/actions/update-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/update-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fieldsToRemove": "string",
  "jobId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/databricks/latest/actions/update-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fieldsToRemove": "string",
    "jobId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fieldsToRemove` | list<string> | yes | Remove top-level fields in the job settings. Removing nested fields is not supported, except for tasks and job clusters (`tasks/task_1`). This field is optional. |
| `jobId` | number | yes | The canonical identifier of the job to update. This field is required. |
| `newSettings` | object | no |  |
| `newSettings.budgetPolicyId` | string | no | The id of the user specified budget policy to use for this job. If not specified, a default budget policy may be applied when creating or modifying the job. See `effective_budget_policy_id` for the budget policy used by this workload. |
| `newSettings.continuous` | object | no |  |
| `newSettings.deployment` | object | no |  |
| `newSettings.description` | string | no | An optional description for the job. The maximum length is 27700 characters in UTF-8 encoding. |
| `newSettings.editMode` | string | no | Edit mode of the job. * `UI_LOCKED`: The job is in a locked UI state and cannot be modified. * `EDITABLE`: The job is in an editable state and can be modified. |
| `newSettings.emailNotifications` | object | no |  |
| `newSettings.environments` | list<string> | no | A list of task execution environment specifications that can be referenced by serverless tasks of this job. For serverless notebook tasks, if the environment_key is not specified, the notebook environment will be used if present. If a jobs environment is specified, it will override the notebook environment. For other serverless tasks, the task environment is required to be specified using environment_key in the task settings. |
| `newSettings.format` | string | no |  |
| `newSettings.gitSource` | object | no | An optional specification for a remote Git repository containing the source code used by tasks. Version-controlled source code is supported by notebook, dbt, Python script, and SQL File tasks. If `git_source` is set, these tasks retrieve the file from the remote repository by default. However, this behavior can be overridden by setting `source` to `WORKSPACE` on the task. Note: dbt and SQL File tasks support only version-controlled sources. If dbt or SQL File tasks are used, `git_source` must be defined on the job. |
| `newSettings.health` | object | no | An optional set of health rules that can be defined for this job. |
| `newSettings.jobClusters` | list<string> | no | A list of job cluster specifications that can be shared and reused by tasks of this job. Libraries cannot be declared in a shared job cluster. You must declare dependent libraries in task settings. |
| `newSettings.maxConcurrentRuns` | number | no | An optional maximum allowed number of concurrent runs of the job. Set this value if you want to be able to execute multiple runs of the same job concurrently. This is useful for example if you trigger your job on a frequent schedule and want to allow consecutive runs to overlap with each other, or if you want to trigger multiple runs which differ by their input parameters. This setting affects only new runs. For example, suppose the jobâs concurrency is 4 and there are 4 concurrent active runs. Then setting the concurrency to 3 wonât kill any of the active runs. However, from then on, new runs are skipped unless there are fewer than 3 active runs. This value cannot exceed 1000. Setting this value to `0` causes all new runs to be skipped. |
| `newSettings.name` | string | no | An optional name for the job. The maximum length is 4096 bytes in UTF-8 encoding. |
| `newSettings.notificationSettings` | object | no |  |
| `newSettings.parameters` | list<string> | no | Job-level parameter definitions |
| `newSettings.performanceTarget` | string | no | PerformanceTarget defines how performant (lower latency) or cost efficient the execution of run on serverless compute should be. The performance mode on the job or pipeline should map to a performance setting that is passed to Cluster Manager (see cluster-common PerformanceTarget). |
| `newSettings.queue` | object | no |  |
| `newSettings.runAs` | object | no | Write-only setting. Specifies the user or service principal that the job runs as. If not specified, the job runs as the user who created the job. Either `user_name` or `service_principal_name` should be specified. If not, an error is thrown. |
| `newSettings.schedule` | object | no |  |
| `newSettings.tags` | object | no | A map of tags associated with the job. These are forwarded to the cluster as cluster tags for jobs clusters, and are subject to the same limitations as cluster tags. A maximum of 25 tags can be added to the job. |
| `newSettings.tasks` | list<string> | no | A list of task specifications to be executed by this job. It supports up to 1000 elements in write endpoints (:method:jobs/create, :method:jobs/reset, :method:jobs/update, :method:jobs/submit). Read endpoints return only 100 tasks. If more than 100 tasks are available, you can paginate through them using :method:jobs/get. Use the `next_page_token` field at the object root to determine if more results are available. |
| `newSettings.timeoutSeconds` | number | no | An optional timeout applied to each run of this job. A value of `0` means no timeout. |
| `newSettings.trigger` | object | no |  |
| `newSettings.webhookNotifications` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_time": 1,
      "job_id": 1,
      "run_as_user_name": "Ava Chen",
      "settings": {
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_time` | number | Epoch milliseconds when the job was created. |
| `job_id` | number | Canonical identifier for the job. |
| `run_as_user_name` | string | Identity the job runs as. |
| `settings.name` | string | Job name from the settings payload. |

## Native endpoint

Through the native Databricks API, this operation is `POST {{credentials.host}}/api/2.2/jobs/update` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-job.md) for the provider-specific parameters and requirements.

