# Create Job with Databricks

Creates a new job in the Databricks workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `{host}/api/2.2/jobs/create`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Create Job](https://docs.databricks.com/api/workspace/jobs/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access_control_list` | body | `list<string>` | yes | List of permissions to set on the job. |
| `cluster_name` | body | `string` | no | Cluster name requested by the user. This doesn't have to be unique. If not specified at creation, the cluster name will be an empty string. For job clusters, the cluster name is automatically set based on the job and job run IDs. |
| `cluster_name` | body | `string` | no | Cluster name requested by the user. This doesn't have to be unique. If not specified at creation, the cluster name will be an empty string. For job clusters, the cluster name is automatically set based on the job and job run IDs. |
| `cluster_name` | body | `string` | no | Cluster name requested by the user. This doesn't have to be unique. If not specified at creation, the cluster name will be an empty string. For job clusters, the cluster name is automatically set based on the job and job run IDs. |
| `budget_policy_id` | body | `string` | no | The id of the user specified budget policy to use for this job. If not specified, a default budget policy may be applied when creating or modifying the job. See `effective_budget_policy_id` for the budget policy used by this workload. |
| `group_name` | body | `string` | no | name of the group |
| `continuous` | body | `object` | no | — |
| `permission_level` | body | `string` | no | Permission level |
| `pause_status` | body | `string` | no | — |
| `service_principal_name` | body | `string` | no | application ID of a service principal |
| `task_retry_mode` | body | `string` | no | task retry mode of the continuous job * NEVER: The failed task will not be retried. * ON_FAILURE: Retry a failed task if at least one other task in the job is still running its first attempt. When this condition is no longer met or the retry limit is reached, the job run is cancelled and a new run is started. |
| `user_name` | body | `string` | no | name of the user |
| `deployment` | body | `object` | no | — |
| `deployment.kind` | body | `string` | yes | * `BUNDLE`: The job is managed by Databricks Asset Bundle. * `SYSTEM_MANAGED`: The job is managed by Databricks and is read-only. |
| `metadata_file_path` | body | `string` | no | Path of the file that contains deployment metadata. |
| `description` | body | `string` | no | An optional description for the job. The maximum length is 27700 characters in UTF-8 encoding. |
| `edit_mode` | body | `string` | no | Edit mode of the job.  * `UI_LOCKED`: The job is in a locked UI state and cannot be modified. * `EDITABLE`: The job is in an editable state and can be modified. |
| `email_notifications` | body | `object` | no | — |
| `no_alert_for_skipped_runs` | body | `boolean` | no | If true, do not send email to recipients specified in `on_failure` if the run is skipped. This field is `deprecated`. Please use the `notification_settings.no_alert_for_skipped_runs` field. |
| `on_duration_warning_threshold_exceeded` | body | `list<string>` | no | A list of email addresses to be notified when the duration of a run exceeds the threshold specified for the `RUN_DURATION_SECONDS` metric in the `health` field. If no rule for the `RUN_DURATION_SECONDS` metric is specified in the `health` field for the job, notifications are not sent. |
| `on_failure` | body | `list<string>` | no | A list of email addresses to be notified when a run unsuccessfully completes. A run is considered to have completed unsuccessfully if it ends with an `INTERNAL_ERROR` `life_cycle_state` or a `FAILED`, or `TIMED_OUT` result_state. If this is not specified on job creation, reset, or update the list is empty, and notifications are not sent. |
| `on_start` | body | `list<string>` | no | A list of email addresses to be notified when a run begins. If not specified on job creation, reset, or update, the list is empty, and notifications are not sent. |
| `on_streaming_backlog_exceeded` | body | `list<string>` | no | A list of email addresses to notify when any streaming backlog thresholds are exceeded for any stream. Streaming backlog thresholds can be set in the `health` field using the following metrics: `STREAMING_BACKLOG_BYTES`, `STREAMING_BACKLOG_RECORDS`, `STREAMING_BACKLOG_SECONDS`, or `STREAMING_BACKLOG_FILES`. Alerting is based on the 10-minute average of these metrics. If the issue persists, notifications are resent every 30 minutes. |
| `on_success` | body | `list<string>` | no | A list of email addresses to be notified when a run successfully completes. A run is considered to have completed successfully if it ends with a `TERMINATED` `life_cycle_state` and a `SUCCESS` result_state. If not specified on job creation, reset, or update, the list is empty, and notifications are not sent. |
| `environments` | body | `list<string>` | yes | A list of task execution environment specifications that can be referenced by serverless tasks of this job. For serverless notebook tasks, if the environment_key is not specified, the notebook environment will be used if present. If a jobs environment is specified, it will override the notebook environment. For other serverless tasks, the task environment is required to be specified using environment_key in the task settings. |
| `format` | body | `string` | no | — |
| `git_source` | body | `object` | no | An optional specification for a remote Git repository containing the source code used by tasks. Version-controlled source code is supported by notebook, dbt, Python script, and SQL File tasks.  If `git_source` is set, these tasks retrieve the file from the remote repository by default. However, this behavior can be overridden by setting `source` to `WORKSPACE` on the task.  Note: dbt and SQL File tasks support only version-controlled sources. If dbt or SQL File tasks are used, `git_source` must be defined on the job. |
| `git_branch` | body | `string` | no | Name of the branch to be checked out and used by this job. This field cannot be specified in conjunction with git_tag or git_commit. |
| `git_commit` | body | `string` | no | Commit to be checked out and used by this job. This field cannot be specified in conjunction with git_branch or git_tag. |
| `environment_key` | body | `string` | yes | The key of an environment. It has to be unique within a job. |
| `git_provider` | body | `string` | yes | — |
| `environments[].spec` | body | `object` | no | The environment entity used to preserve serverless environment side panel, jobs' environment for non-notebook task, and DLT's environment for classic and serverless pipelines. In this minimal environment spec, only pip and java dependencies are supported. |
| `git_snapshot` | body | `object` | no | Read-only state of the remote repository at the time the job was run. This field is only included on job runs. |
| `base_environment` | body | `string` | no | The `base_environment` key refers to an `env.yaml` file that specifies an environment version and a collection of dependencies required for the environment setup. This `env.yaml` file may itself include a `base_environment` reference pointing to another `env_1.yaml` file. However, when used as a base environment, `env_1.yaml` (or further nested references) will not be processed or included in the final environment, meaning that the resolution of `base_environment` references is not recursive. |
| `git_tag` | body | `string` | no | Name of the tag to be checked out and used by this job. This field cannot be specified in conjunction with git_branch or git_commit. |
| `environments[].spec.client` | body | `string` | no | Use `environment_version` instead. |
| `git_url` | body | `string` | yes | URL of the repository to be cloned by this job. |
| `environments[].spec.dependencies` | body | `list<string>` | yes | List of pip dependencies, as supported by the version of pip in this environment. Each dependency is a valid pip requirements file line per https://pip.pypa.io/en/stable/reference/requirements-file-format/. Allowed dependencies include a requirement specifier, an archive URL, a local project path (such as WSFS or UC Volumes in Databricks), or a VCS project URL. |
| `sparse_checkout` | body | `object` | no | — |
| `environment_version` | body | `string` | no | Either `environment_version` or `base_environment` needs to be provided. Environment version used by the environment. Each version comes with a specific Python version and a set of Python packages. The version is a string, consisting of an integer. See https://docs.databricks.com/aws/release-notes/serverless/#serverless-environment-versions. |
| `health` | body | `object` | no | An optional set of health rules that can be defined for this job. |
| `health.rules` | body | `list<string>` | no | — |
| `java_dependencies` | body | `list<string>` | yes | List of java dependencies. Each dependency is a string representing a java library path. For example: `/Volumes/path/to/test.jar`. See https://docs.databricks.com/aws/en/jobs/jar. |
| `job_clusters` | body | `list<string>` | yes | A list of job cluster specifications that can be shared and reused by tasks of this job. Libraries cannot be declared in a shared job cluster. You must declare dependent libraries in task settings. |
| `max_concurrent_runs` | body | `number` | no | An optional maximum allowed number of concurrent runs of the job. Set this value if you want to be able to execute multiple runs of the same job concurrently. This is useful for example if you trigger your job on a frequent schedule and want to allow consecutive runs to overlap with each other, or if you want to trigger multiple runs which differ by their input parameters. This setting affects only new runs. For example, suppose the jobâs concurrency is 4 and there are 4 concurrent active runs. Then setting the concurrency to 3 wonât kill any of the active runs. However, from then on, new runs are skipped unless there are fewer than 3 active runs. This value cannot exceed 1000. Setting this value to `0` causes all new runs to be skipped. |
| `name` | body | `string` | no | An optional name for the job. The maximum length is 4096 bytes in UTF-8 encoding. |
| `notification_settings` | body | `object` | no | — |
| `no_alert_for_canceled_runs` | body | `boolean` | no | If true, do not send notifications to recipients specified in `on_failure` if the run is canceled. |
| `no_alert_for_skipped_runs` | body | `boolean` | no | If true, do not send notifications to recipients specified in `on_failure` if the run is skipped. |
| `parameters` | body | `list<string>` | yes | Job-level parameter definitions |
| `used_commit` | body | `string` | no | Commit that was used to execute the run. If git_branch was specified, this points to the HEAD of the branch at the time of the run; if git_tag was specified, this points to the commit the tag points to. |
| `performance_target` | body | `string` | no | PerformanceTarget defines how performant (lower latency) or cost efficient the execution of run on serverless compute should be. The performance mode on the job or pipeline should map to a performance setting that is passed to Cluster Manager (see cluster-common PerformanceTarget). |
| `queue` | body | `object` | no | — |
| `queue.enabled` | body | `boolean` | yes | If true, enable queueing for the job. This is a required field. |
| `gitSource.sparseCheckout.patterns` | body | `list<string>` | yes | List of patterns to include for sparse checkout. |
| `run_as` | body | `object` | no | Write-only setting. Specifies the user or service principal that the job runs as. If not specified, the job runs as the user who created the job.  Either `user_name` or `service_principal_name` should be specified. If not, an error is thrown. |
| `service_principal_name` | body | `string` | no | Application ID of an active service principal. Setting this field requires the `servicePrincipal/user` role. |
| `user_name` | body | `string` | no | The email of an active workspace user. Non-admin users can only set this field to their own email. |
| `health.rules[].metric` | body | `string` | yes | Specifies the health metric that is being evaluated for a particular health rule.  * `RUN_DURATION_SECONDS`: Expected total time for a run in seconds. * `STREAMING_BACKLOG_BYTES`: An estimate of the maximum bytes of data waiting to be consumed across all streams. This metric is in Public Preview. * `STREAMING_BACKLOG_RECORDS`: An estimate of the maximum offset lag across all streams. This metric is in Public Preview. * `STREAMING_BACKLOG_SECONDS`: An estimate of the maximum consumer delay across all streams. This metric is in Public Preview. * `STREAMING_BACKLOG_FILES`: An estimate of the maximum number of outstanding files across all streams. This metric is in Public Preview. |
| `schedule` | body | `object` | no | — |
| `health.rules[].op` | body | `string` | yes | Specifies the operator used to compare the health metric value with the specified threshold. |
| `pause_status` | body | `string` | no | — |
| `health.rules[].value` | body | `number` | yes | Specifies the threshold value that the health metric should obey to satisfy the health rule. |
| `quartz_cron_expression` | body | `string` | yes | A Cron expression using Quartz syntax that describes the schedule for a job. See [Cron Trigger](http://www.quartz-scheduler.org/documentation/quartz-2.3.0/tutorials/crontrigger.html) for details. This field is required. |
| `timezone_id` | body | `string` | yes | A Java timezone ID. The schedule for a job is resolved with respect to this timezone. See [Java TimeZone](https://docs.oracle.com/javase/7/docs/api/java/util/TimeZone.html) for details. This field is required. |
| `job_cluster_key` | body | `string` | yes | A unique name for the job cluster. This field is required and must be unique within the job. `JobTaskSettings` may refer to this field to determine which cluster to launch for the task execution. |
| `tags` | body | `object` | no | A map of tags associated with the job. These are forwarded to the cluster as cluster tags for jobs clusters, and are subject to the same limitations as cluster tags. A maximum of 25 tags can be added to the job. |
| `new_cluster` | body | `object` | yes | Contains a snapshot of the latest user specified settings that were used to create/edit the cluster. |
| `tasks` | body | `list<string>` | yes | A list of task specifications to be executed by this job. It supports up to 1000 elements in write endpoints (:method:jobs/create, :method:jobs/reset, :method:jobs/update, :method:jobs/submit). Read endpoints return only 100 tasks. If more than 100 tasks are available, you can paginate through them using :method:jobs/get. Use the `next_page_token` field at the object root to determine if more results are available. |
| `apply_policy_default_values` | body | `boolean` | no | When set to true, fixed and default values from the policy will be used for fields that are omitted. When set to false, only fixed values from the policy will be applied. |
| `timeout_seconds` | body | `number` | no | An optional timeout applied to each run of this job. A value of `0` means no timeout. |
| `jobClusters[].newCluster.autoscale` | body | `object` | no | — |
| `trigger` | body | `object` | no | — |
| `file_arrival` | body | `object` | no | — |
| `max_workers` | body | `number` | no | The maximum number of workers to which the cluster can scale up when overloaded. Note that `max_workers` must be strictly greater than `min_workers`. |
| `min_workers` | body | `number` | no | The minimum number of workers to which the cluster can scale down when underutilized. It is also the initial number of workers the cluster will have after creation. |
| `pause_status` | body | `string` | no | — |
| `autotermination_minutes` | body | `number` | no | Automatically terminates the cluster after it is inactive for this time in minutes. If not set, this cluster will not be automatically terminated. If specified, the threshold must be between 10 and 10000 minutes. Users can also set this value to 0 to explicitly disable automatic termination. |
| `trigger.periodic` | body | `object` | no | — |
| `aws_attributes` | body | `object` | no | Attributes set during cluster creation which are related to Amazon Web Services. |
| `table_update` | body | `object` | no | — |
| `jobClusters[].newCluster.awsAttributes.availability` | body | `string` | no | Availability type used for all subsequent nodes past the `first_on_demand` ones.  Note: If `first_on_demand` is zero, this availability type will be used for the entire cluster. |
| `webhook_notifications` | body | `object` | no | — |
| `ebs_volume_count` | body | `number` | no | The number of volumes launched for each instance. Users can choose up to 10 volumes. This feature is only enabled for supported node types. Legacy node types cannot specify custom EBS volumes. For node types with no instance store, at least one EBS volume needs to be specified; otherwise, cluster creation will fail.  These EBS volumes will be mounted at `/ebs0`, `/ebs1`, and etc. Instance store volumes will be mounted at `/local_disk0`, `/local_disk1`, and etc.  If EBS volumes are attached, Databricks will configure Spark to use only the EBS volumes for scratch storage because heterogenously sized scratch devices can lead to inefficient disk utilization. If no EBS volumes are attached, Databricks will configure Spark to use instance store volumes.  Please note that if EBS volumes are specified, then the Spark configuration `spark.local.dir` will be overridden. |
| `on_duration_warning_threshold_exceeded` | body | `list<string>` | no | An optional list of system notification IDs to call when the duration of a run exceeds the threshold specified for the `RUN_DURATION_SECONDS` metric in the `health` field. A maximum of 3 destinations can be specified for the `on_duration_warning_threshold_exceeded` property. |
| `ebs_volume_iops` | body | `number` | no | If using gp3 volumes, what IOPS to use for the disk. If this is not set, the maximum performance of a gp2 volume with the same volume size will be used. |
| `on_failure` | body | `list<string>` | no | An optional list of system notification IDs to call when the run fails. A maximum of 3 destinations can be specified for the `on_failure` property. |
| `ebs_volume_size` | body | `number` | no | The size of each EBS volume (in GiB) launched for each instance. For general purpose SSD, this value must be within the range 100 - 4096. For throughput optimized HDD, this value must be within the range 500 - 4096. |
| `on_start` | body | `list<string>` | no | An optional list of system notification IDs to call when the run starts. A maximum of 3 destinations can be specified for the `on_start` property. |
| `ebs_volume_throughput` | body | `number` | no | If using gp3 volumes, what throughput to use for the disk. If this is not set, the maximum performance of a gp2 volume with the same volume size will be used. |
| `on_streaming_backlog_exceeded` | body | `list<string>` | no | An optional list of system notification IDs to call when any streaming backlog thresholds are exceeded for any stream. Streaming backlog thresholds can be set in the `health` field using the following metrics: `STREAMING_BACKLOG_BYTES`, `STREAMING_BACKLOG_RECORDS`, `STREAMING_BACKLOG_SECONDS`, or `STREAMING_BACKLOG_FILES`. Alerting is based on the 10-minute average of these metrics. If the issue persists, notifications are resent every 30 minutes. A maximum of 3 destinations can be specified for the `on_streaming_backlog_exceeded` property. |
| `ebs_volume_type` | body | `string` | no | All EBS volume types that Databricks supports. See https://aws.amazon.com/ebs/details/ for details. |
| `on_success` | body | `list<string>` | no | An optional list of system notification IDs to call when the run completes successfully. A maximum of 3 destinations can be specified for the `on_success` property. |
| `first_on_demand` | body | `number` | no | The first `first_on_demand` nodes of the cluster will be placed on on-demand instances. If this value is greater than 0, the cluster driver node in particular will be placed on an on-demand instance. If this value is greater than or equal to the current cluster size, all nodes will be placed on on-demand instances. If this value is less than the current cluster size, `first_on_demand` nodes will be placed on on-demand instances and the remainder will be placed on `availability` instances. Note that this value does not affect cluster size and cannot currently be mutated over the lifetime of a cluster. |
| `instance_profile_arn` | body | `string` | no | Nodes for this cluster will only be placed on AWS instances with this instance profile. If ommitted, nodes will be placed on instances without an IAM instance profile. The instance profile must have previously been added to the Databricks environment by an account administrator.  This feature may only be available to certain customer plans. |
| `spot_bid_price_percent` | body | `number` | no | The bid price for AWS spot instances, as a percentage of the corresponding instance type's on-demand price. For example, if this field is set to 50, and the cluster needs a new `r3.xlarge` spot instance, then the bid price is half of the price of on-demand `r3.xlarge` instances. Similarly, if this field is set to 200, the bid price is twice the price of on-demand `r3.xlarge` instances. If not specified, the default value is 100. When spot instances are requested for this cluster, only spot instances whose bid price percentage matches this field will be considered. Note that, for safety, we enforce this field to be no more than 10000. |
| `zone_id` | body | `string` | no | Identifier for the availability zone/datacenter in which the cluster resides. This string will be of a form like "us-west-2a". The provided availability zone must be in the same region as the Databricks deployment. For example, "us-west-2a" is not a valid zone id if the Databricks deployment resides in the "us-east-1" region. This is an optional field at cluster creation, and if not specified, the zone "auto" will be used. If the zone specified is "auto", will try to place cluster in a zone with high availability, and will retry placement in a different AZ if there is not enough capacity.  The list of available zones as well as the default value can be found by using the `List Zones` method. |
| `cluster_log_conf` | body | `object` | no | Cluster log delivery config |
| `jobClusters[].newCluster.clusterLogConf.dbfs` | body | `object` | no | A storage location in DBFS |
| `jobClusters[].newCluster.clusterLogConf.s3` | body | `object` | no | A storage location in Amazon S3 |
| `jobClusters[].newCluster.clusterLogConf.volumes` | body | `object` | no | A storage location back by UC Volumes. |
