# Databricks: Create Job

Creates a new job in the Databricks workspace.

```
POST https://connect.mindcloud.co/v1/universal/databricks/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accessControlList": "string",
  "deployment.kind": "string",
  "environments": "string",
  "environments[].environmentKey": "string",
  "gitSource.gitProvider": "string",
  "gitSource.gitUrl": "https://example.com",
  "environments[].spec.dependencies": "string",
  "environments[].spec.javaDependencies": "string",
  "jobClusters": "string",
  "parameters": "string",
  "queue.enabled": true,
  "gitSource.sparseCheckout.patterns": "string",
  "health.rules[].metric": "string",
  "health.rules[].op": "string",
  "health.rules[].value": 1,
  "schedule.quartzCronExpression": "string",
  "schedule.timezoneId": "string",
  "jobClusters[].jobClusterKey": "string",
  "jobClusters[].newCluster": {},
  "tasks": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/databricks/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accessControlList": "string",
    "deployment.kind": "string",
    "environments": "string",
    "environments[].environmentKey": "string",
    "gitSource.gitProvider": "string",
    "gitSource.gitUrl": "https://example.com",
    "environments[].spec.dependencies": "string",
    "environments[].spec.javaDependencies": "string",
    "jobClusters": "string",
    "parameters": "string",
    "queue.enabled": true,
    "gitSource.sparseCheckout.patterns": "string",
    "health.rules[].metric": "string",
    "health.rules[].op": "string",
    "health.rules[].value": 1,
    "schedule.quartzCronExpression": "string",
    "schedule.timezoneId": "string",
    "jobClusters[].jobClusterKey": "string",
    "jobClusters[].newCluster": {},
    "tasks": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accessControlList` | list<string> | yes | List of permissions to set on the job. |
| `jobClusters[].newCluster.clusterName` | string | no | Cluster name requested by the user. This doesn't have to be unique. If not specified at creation, the cluster name will be an empty string. For job clusters, the cluster name is automatically set based on the job and job run IDs. |
| `jobClusters[].newCluster.clusterName` | string | no | Cluster name requested by the user. This doesn't have to be unique. If not specified at creation, the cluster name will be an empty string. For job clusters, the cluster name is automatically set based on the job and job run IDs. |
| `jobClusters[].newCluster.clusterName` | string | no | Cluster name requested by the user. This doesn't have to be unique. If not specified at creation, the cluster name will be an empty string. For job clusters, the cluster name is automatically set based on the job and job run IDs. |
| `accessControlList[].groupName` | string | no | name of the group |
| `budgetPolicyId` | string | no | The id of the user specified budget policy to use for this job. If not specified, a default budget policy may be applied when creating or modifying the job. See `effective_budget_policy_id` for the budget policy used by this workload. |
| `accessControlList[].permissionLevel` | string | no | Permission level |
| `continuous` | object | no |  |
| `accessControlList[].servicePrincipalName` | string | no | application ID of a service principal |
| `continuous.pauseStatus` | string | no |  |
| `accessControlList[].userName` | string | no | name of the user |
| `continuous.taskRetryMode` | string | no | task retry mode of the continuous job * NEVER: The failed task will not be retried. * ON_FAILURE: Retry a failed task if at least one other task in the job is still running its first attempt. When this condition is no longer met or the retry limit is reached, the job run is cancelled and a new run is started. |
| `deployment` | object | no |  |
| `deployment.kind` | string | yes | * `BUNDLE`: The job is managed by Databricks Asset Bundle. * `SYSTEM_MANAGED`: The job is managed by Databricks and is read-only. |
| `deployment.metadataFilePath` | string | no | Path of the file that contains deployment metadata. |
| `description` | string | no | An optional description for the job. The maximum length is 27700 characters in UTF-8 encoding. |
| `editMode` | string | no | Edit mode of the job. * `UI_LOCKED`: The job is in a locked UI state and cannot be modified. * `EDITABLE`: The job is in an editable state and can be modified. |
| `emailNotifications` | object | no |  |
| `emailNotifications.noAlertForSkippedRuns` | boolean | no | If true, do not send email to recipients specified in `on_failure` if the run is skipped. This field is `deprecated`. Please use the `notification_settings.no_alert_for_skipped_runs` field. |
| `emailNotifications.onDurationWarningThresholdExceeded` | list<string> | no | A list of email addresses to be notified when the duration of a run exceeds the threshold specified for the `RUN_DURATION_SECONDS` metric in the `health` field. If no rule for the `RUN_DURATION_SECONDS` metric is specified in the `health` field for the job, notifications are not sent. |
| `emailNotifications.onFailure` | list<string> | no | A list of email addresses to be notified when a run unsuccessfully completes. A run is considered to have completed unsuccessfully if it ends with an `INTERNAL_ERROR` `life_cycle_state` or a `FAILED`, or `TIMED_OUT` result_state. If this is not specified on job creation, reset, or update the list is empty, and notifications are not sent. |
| `emailNotifications.onStart` | list<string> | no | A list of email addresses to be notified when a run begins. If not specified on job creation, reset, or update, the list is empty, and notifications are not sent. |
| `emailNotifications.onStreamingBacklogExceeded` | list<string> | no | A list of email addresses to notify when any streaming backlog thresholds are exceeded for any stream. Streaming backlog thresholds can be set in the `health` field using the following metrics: `STREAMING_BACKLOG_BYTES`, `STREAMING_BACKLOG_RECORDS`, `STREAMING_BACKLOG_SECONDS`, or `STREAMING_BACKLOG_FILES`. Alerting is based on the 10-minute average of these metrics. If the issue persists, notifications are resent every 30 minutes. |
| `emailNotifications.onSuccess` | list<string> | no | A list of email addresses to be notified when a run successfully completes. A run is considered to have completed successfully if it ends with a `TERMINATED` `life_cycle_state` and a `SUCCESS` result_state. If not specified on job creation, reset, or update, the list is empty, and notifications are not sent. |
| `environments` | list<string> | yes | A list of task execution environment specifications that can be referenced by serverless tasks of this job. For serverless notebook tasks, if the environment_key is not specified, the notebook environment will be used if present. If a jobs environment is specified, it will override the notebook environment. For other serverless tasks, the task environment is required to be specified using environment_key in the task settings. |
| `format` | string | no |  |
| `gitSource` | object | no | An optional specification for a remote Git repository containing the source code used by tasks. Version-controlled source code is supported by notebook, dbt, Python script, and SQL File tasks. If `git_source` is set, these tasks retrieve the file from the remote repository by default. However, this behavior can be overridden by setting `source` to `WORKSPACE` on the task. Note: dbt and SQL File tasks support only version-controlled sources. If dbt or SQL File tasks are used, `git_source` must be defined on the job. |
| `gitSource.gitBranch` | string | no | Name of the branch to be checked out and used by this job. This field cannot be specified in conjunction with git_tag or git_commit. |
| `gitSource.gitCommit` | string | no | Commit to be checked out and used by this job. This field cannot be specified in conjunction with git_branch or git_tag. |
| `environments[].environmentKey` | string | yes | The key of an environment. It has to be unique within a job. |
| `gitSource.gitProvider` | string | yes |  |
| `environments[].spec` | object | no | The environment entity used to preserve serverless environment side panel, jobs' environment for non-notebook task, and DLT's environment for classic and serverless pipelines. In this minimal environment spec, only pip and java dependencies are supported. |
| `gitSource.gitSnapshot` | object | no | Read-only state of the remote repository at the time the job was run. This field is only included on job runs. |
| `environments[].spec.baseEnvironment` | string | no | The `base_environment` key refers to an `env.yaml` file that specifies an environment version and a collection of dependencies required for the environment setup. This `env.yaml` file may itself include a `base_environment` reference pointing to another `env_1.yaml` file. However, when used as a base environment, `env_1.yaml` (or further nested references) will not be processed or included in the final environment, meaning that the resolution of `base_environment` references is not recursive. |
| `gitSource.gitTag` | string | no | Name of the tag to be checked out and used by this job. This field cannot be specified in conjunction with git_branch or git_commit. |
| `environments[].spec.client` | string | no | Use `environment_version` instead. |
| `gitSource.gitUrl` | string | yes | URL of the repository to be cloned by this job. |
| `environments[].spec.dependencies` | list<string> | yes | List of pip dependencies, as supported by the version of pip in this environment. Each dependency is a valid pip requirements file line per https://pip.pypa.io/en/stable/reference/requirements-file-format/. Allowed dependencies include a requirement specifier, an archive URL, a local project path (such as WSFS or UC Volumes in Databricks), or a VCS project URL. |
| `gitSource.sparseCheckout` | object | no |  |
| `environments[].spec.environmentVersion` | string | no | Either `environment_version` or `base_environment` needs to be provided. Environment version used by the environment. Each version comes with a specific Python version and a set of Python packages. The version is a string, consisting of an integer. See https://docs.databricks.com/aws/release-notes/serverless/#serverless-environment-versions. |
| `health` | object | no | An optional set of health rules that can be defined for this job. |
| `environments[].spec.javaDependencies` | list<string> | yes | List of java dependencies. Each dependency is a string representing a java library path. For example: `/Volumes/path/to/test.jar`. See https://docs.databricks.com/aws/en/jobs/jar. |
| `health.rules` | list<string> | no |  |
| `jobClusters` | list<string> | yes | A list of job cluster specifications that can be shared and reused by tasks of this job. Libraries cannot be declared in a shared job cluster. You must declare dependent libraries in task settings. |
| `maxConcurrentRuns` | number | no | An optional maximum allowed number of concurrent runs of the job. Set this value if you want to be able to execute multiple runs of the same job concurrently. This is useful for example if you trigger your job on a frequent schedule and want to allow consecutive runs to overlap with each other, or if you want to trigger multiple runs which differ by their input parameters. This setting affects only new runs. For example, suppose the jobâs concurrency is 4 and there are 4 concurrent active runs. Then setting the concurrency to 3 wonât kill any of the active runs. However, from then on, new runs are skipped unless there are fewer than 3 active runs. This value cannot exceed 1000. Setting this value to `0` causes all new runs to be skipped. |
| `name` | string | no | An optional name for the job. The maximum length is 4096 bytes in UTF-8 encoding. |
| `notificationSettings` | object | no |  |
| `notificationSettings.noAlertForCanceledRuns` | boolean | no | If true, do not send notifications to recipients specified in `on_failure` if the run is canceled. |
| `notificationSettings.noAlertForSkippedRuns` | boolean | no | If true, do not send notifications to recipients specified in `on_failure` if the run is skipped. |
| `gitSource.gitSnapshot.usedCommit` | string | no | Commit that was used to execute the run. If git_branch was specified, this points to the HEAD of the branch at the time of the run; if git_tag was specified, this points to the commit the tag points to. |
| `parameters` | list<string> | yes | Job-level parameter definitions |
| `performanceTarget` | string | no | PerformanceTarget defines how performant (lower latency) or cost efficient the execution of run on serverless compute should be. The performance mode on the job or pipeline should map to a performance setting that is passed to Cluster Manager (see cluster-common PerformanceTarget). |
| `queue` | object | no |  |
| `queue.enabled` | boolean | yes | If true, enable queueing for the job. This is a required field. |
| `gitSource.sparseCheckout.patterns` | list<string> | yes | List of patterns to include for sparse checkout. |
| `runAs` | object | no | Write-only setting. Specifies the user or service principal that the job runs as. If not specified, the job runs as the user who created the job. Either `user_name` or `service_principal_name` should be specified. If not, an error is thrown. |
| `runAs.servicePrincipalName` | string | no | Application ID of an active service principal. Setting this field requires the `servicePrincipal/user` role. |
| `runAs.userName` | string | no | The email of an active workspace user. Non-admin users can only set this field to their own email. |
| `health.rules[].metric` | string | yes | Specifies the health metric that is being evaluated for a particular health rule. * `RUN_DURATION_SECONDS`: Expected total time for a run in seconds. * `STREAMING_BACKLOG_BYTES`: An estimate of the maximum bytes of data waiting to be consumed across all streams. This metric is in Public Preview. * `STREAMING_BACKLOG_RECORDS`: An estimate of the maximum offset lag across all streams. This metric is in Public Preview. * `STREAMING_BACKLOG_SECONDS`: An estimate of the maximum consumer delay across all streams. This metric is in Public Preview. * `STREAMING_BACKLOG_FILES`: An estimate of the maximum number of outstanding files across all streams. This metric is in Public Preview. |
| `schedule` | object | no |  |
| `health.rules[].op` | string | yes | Specifies the operator used to compare the health metric value with the specified threshold. |
| `schedule.pauseStatus` | string | no |  |
| `health.rules[].value` | number | yes | Specifies the threshold value that the health metric should obey to satisfy the health rule. |
| `schedule.quartzCronExpression` | string | yes | A Cron expression using Quartz syntax that describes the schedule for a job. See [Cron Trigger](http://www.quartz-scheduler.org/documentation/quartz-2.3.0/tutorials/crontrigger.html) for details. This field is required. |
| `schedule.timezoneId` | string | yes | A Java timezone ID. The schedule for a job is resolved with respect to this timezone. See [Java TimeZone](https://docs.oracle.com/javase/7/docs/api/java/util/TimeZone.html) for details. This field is required. |
| `jobClusters[].jobClusterKey` | string | yes | A unique name for the job cluster. This field is required and must be unique within the job. `JobTaskSettings` may refer to this field to determine which cluster to launch for the task execution. |
| `tags` | object | no | A map of tags associated with the job. These are forwarded to the cluster as cluster tags for jobs clusters, and are subject to the same limitations as cluster tags. A maximum of 25 tags can be added to the job. |
| `jobClusters[].newCluster` | object | yes | Contains a snapshot of the latest user specified settings that were used to create/edit the cluster. |
| `tasks` | list<string> | yes | A list of task specifications to be executed by this job. It supports up to 1000 elements in write endpoints (:method:jobs/create, :method:jobs/reset, :method:jobs/update, :method:jobs/submit). Read endpoints return only 100 tasks. If more than 100 tasks are available, you can paginate through them using :method:jobs/get. Use the `next_page_token` field at the object root to determine if more results are available. |
| `jobClusters[].newCluster.applyPolicyDefaultValues` | boolean | no | When set to true, fixed and default values from the policy will be used for fields that are omitted. When set to false, only fixed values from the policy will be applied. |
| `timeoutSeconds` | number | no | An optional timeout applied to each run of this job. A value of `0` means no timeout. |
| `jobClusters[].newCluster.autoscale` | object | no |  |
| `trigger` | object | no |  |
| `jobClusters[].newCluster.autoscale.maxWorkers` | number | no | The maximum number of workers to which the cluster can scale up when overloaded. Note that `max_workers` must be strictly greater than `min_workers`. |
| `trigger.fileArrival` | object | no |  |
| `jobClusters[].newCluster.autoscale.minWorkers` | number | no | The minimum number of workers to which the cluster can scale down when underutilized. It is also the initial number of workers the cluster will have after creation. |
| `trigger.pauseStatus` | string | no |  |
| `jobClusters[].newCluster.autoterminationMinutes` | number | no | Automatically terminates the cluster after it is inactive for this time in minutes. If not set, this cluster will not be automatically terminated. If specified, the threshold must be between 10 and 10000 minutes. Users can also set this value to 0 to explicitly disable automatic termination. |
| `trigger.periodic` | object | no |  |
| `jobClusters[].newCluster.awsAttributes` | object | no | Attributes set during cluster creation which are related to Amazon Web Services. |
| `trigger.tableUpdate` | object | no |  |
| `jobClusters[].newCluster.awsAttributes.availability` | string | no | Availability type used for all subsequent nodes past the `first_on_demand` ones. Note: If `first_on_demand` is zero, this availability type will be used for the entire cluster. |
| `webhookNotifications` | object | no |  |
| `jobClusters[].newCluster.awsAttributes.ebsVolumeCount` | number | no | The number of volumes launched for each instance. Users can choose up to 10 volumes. This feature is only enabled for supported node types. Legacy node types cannot specify custom EBS volumes. For node types with no instance store, at least one EBS volume needs to be specified; otherwise, cluster creation will fail. These EBS volumes will be mounted at `/ebs0`, `/ebs1`, and etc. Instance store volumes will be mounted at `/local_disk0`, `/local_disk1`, and etc. If EBS volumes are attached, Databricks will configure Spark to use only the EBS volumes for scratch storage because heterogenously sized scratch devices can lead to inefficient disk utilization. If no EBS volumes are attached, Databricks will configure Spark to use instance store volumes. Please note that if EBS volumes are specified, then the Spark configuration `spark.local.dir` will be overridden. |
| `webhookNotifications.onDurationWarningThresholdExceeded` | list<string> | no | An optional list of system notification IDs to call when the duration of a run exceeds the threshold specified for the `RUN_DURATION_SECONDS` metric in the `health` field. A maximum of 3 destinations can be specified for the `on_duration_warning_threshold_exceeded` property. |
| `jobClusters[].newCluster.awsAttributes.ebsVolumeIops` | number | no | If using gp3 volumes, what IOPS to use for the disk. If this is not set, the maximum performance of a gp2 volume with the same volume size will be used. |
| `webhookNotifications.onFailure` | list<string> | no | An optional list of system notification IDs to call when the run fails. A maximum of 3 destinations can be specified for the `on_failure` property. |
| `jobClusters[].newCluster.awsAttributes.ebsVolumeSize` | number | no | The size of each EBS volume (in GiB) launched for each instance. For general purpose SSD, this value must be within the range 100 - 4096. For throughput optimized HDD, this value must be within the range 500 - 4096. |
| `webhookNotifications.onStart` | list<string> | no | An optional list of system notification IDs to call when the run starts. A maximum of 3 destinations can be specified for the `on_start` property. |
| `jobClusters[].newCluster.awsAttributes.ebsVolumeThroughput` | number | no | If using gp3 volumes, what throughput to use for the disk. If this is not set, the maximum performance of a gp2 volume with the same volume size will be used. |
| `webhookNotifications.onStreamingBacklogExceeded` | list<string> | no | An optional list of system notification IDs to call when any streaming backlog thresholds are exceeded for any stream. Streaming backlog thresholds can be set in the `health` field using the following metrics: `STREAMING_BACKLOG_BYTES`, `STREAMING_BACKLOG_RECORDS`, `STREAMING_BACKLOG_SECONDS`, or `STREAMING_BACKLOG_FILES`. Alerting is based on the 10-minute average of these metrics. If the issue persists, notifications are resent every 30 minutes. A maximum of 3 destinations can be specified for the `on_streaming_backlog_exceeded` property. |
| `jobClusters[].newCluster.awsAttributes.ebsVolumeType` | string | no | All EBS volume types that Databricks supports. See https://aws.amazon.com/ebs/details/ for details. |
| `webhookNotifications.onSuccess` | list<string> | no | An optional list of system notification IDs to call when the run completes successfully. A maximum of 3 destinations can be specified for the `on_success` property. |
| `jobClusters[].newCluster.awsAttributes.firstOnDemand` | number | no | The first `first_on_demand` nodes of the cluster will be placed on on-demand instances. If this value is greater than 0, the cluster driver node in particular will be placed on an on-demand instance. If this value is greater than or equal to the current cluster size, all nodes will be placed on on-demand instances. If this value is less than the current cluster size, `first_on_demand` nodes will be placed on on-demand instances and the remainder will be placed on `availability` instances. Note that this value does not affect cluster size and cannot currently be mutated over the lifetime of a cluster. |
| `jobClusters[].newCluster.awsAttributes.instanceProfileArn` | string | no | Nodes for this cluster will only be placed on AWS instances with this instance profile. If ommitted, nodes will be placed on instances without an IAM instance profile. The instance profile must have previously been added to the Databricks environment by an account administrator. This feature may only be available to certain customer plans. |
| `jobClusters[].newCluster.awsAttributes.spotBidPricePercent` | number | no | The bid price for AWS spot instances, as a percentage of the corresponding instance type's on-demand price. For example, if this field is set to 50, and the cluster needs a new `r3.xlarge` spot instance, then the bid price is half of the price of on-demand `r3.xlarge` instances. Similarly, if this field is set to 200, the bid price is twice the price of on-demand `r3.xlarge` instances. If not specified, the default value is 100. When spot instances are requested for this cluster, only spot instances whose bid price percentage matches this field will be considered. Note that, for safety, we enforce this field to be no more than 10000. |
| `jobClusters[].newCluster.awsAttributes.zoneId` | string | no | Identifier for the availability zone/datacenter in which the cluster resides. This string will be of a form like "us-west-2a". The provided availability zone must be in the same region as the Databricks deployment. For example, "us-west-2a" is not a valid zone id if the Databricks deployment resides in the "us-east-1" region. This is an optional field at cluster creation, and if not specified, the zone "auto" will be used. If the zone specified is "auto", will try to place cluster in a zone with high availability, and will retry placement in a different AZ if there is not enough capacity. The list of available zones as well as the default value can be found by using the `List Zones` method. |
| `jobClusters[].newCluster.clusterLogConf` | object | no | Cluster log delivery config |
| `jobClusters[].newCluster.clusterLogConf.dbfs` | object | no | A storage location in DBFS |
| `jobClusters[].newCluster.clusterLogConf.s3` | object | no | A storage location in Amazon S3 |
| `jobClusters[].newCluster.clusterLogConf.volumes` | object | no | A storage location back by UC Volumes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job_id` | number | The canonical identifier for the newly created job. |

## Native endpoint

Through the native Databricks API, this operation is `POST {{credentials.host}}/api/2.2/jobs/create` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

