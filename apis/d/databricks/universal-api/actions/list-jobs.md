# Databricks: List Jobs

Retrieves jobs from the Databricks workspace.

```
GET https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-jobs?${params}`, {
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
| `limit` | number | no | The number of jobs to return. This value must be greater than 0 and less or equal to 100. The default value is 20. |
| `expandTasks` | boolean | no | Whether to include task and cluster details in the response. Note that only the first 100 elements will be shown. Use :method:jobs/get to paginate through all tasks and clusters. |
| `name` | string | no | A filter on the list based on the exact (case insensitive) job name. |
| `pageToken` | string | no | Use `next_page_token` or `prev_page_token` returned from the previous request to list the next or previous page of jobs respectively. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_time": 1,
      "creator_user_name": "Ava Chen",
      "effective_budget_policy_id": "string",
      "has_more": true,
      "job_id": 1,
      "settings": {
        "budget_policy_id": "string",
        "continuous": {
          "pause_status": "string",
          "task_retry_mode": "string"
        },
        "deployment": {
          "kind": "string",
          "metadata_file_path": "string"
        },
        "description": "string",
        "edit_mode": "string",
        "email_notifications": {
          "no_alert_for_skipped_runs": true,
          "on_duration_warning_threshold_exceeded": [
            "ava@example.com"
          ],
          "on_failure": [
            "ava@example.com"
          ],
          "on_start": [
            "ava@example.com"
          ],
          "on_streaming_backlog_exceeded": [
            "ava@example.com"
          ],
          "on_success": [
            "ava@example.com"
          ]
        },
        "environments": [
          {
            "environment_key": "string",
            "spec": {
              "base_environment": "string",
              "client": "string",
              "dependencies": [
                "string"
              ],
              "environment_version": "string",
              "java_dependencies": [
                "string"
              ]
            }
          }
        ],
        "format": "string",
        "git_source": {
          "git_branch": "string",
          "git_commit": "string",
          "git_provider": "string",
          "git_snapshot": {
            "used_commit": "string"
          },
          "git_tag": "string",
          "git_url": "https://example.com",
          "sparse_checkout": {
            "patterns": [
              "string"
            ]
          }
        },
        "health": {
          "rules": [
            {
              "metric": "string",
              "op": "string",
              "value": 1
            }
          ]
        },
        "job_clusters": [
          {
            "job_cluster_key": "string",
            "new_cluster": {
              "apply_policy_default_values": true,
              "autoscale": {
                "max_workers": 1,
                "min_workers": 1
              },
              "autotermination_minutes": 1,
              "aws_attributes": {
                "availability": "string",
                "ebs_volume_count": 1,
                "ebs_volume_iops": 1,
                "ebs_volume_size": 1,
                "ebs_volume_throughput": 1,
                "ebs_volume_type": "string",
                "first_on_demand": 1,
                "instance_profile_arn": "string",
                "spot_bid_price_percent": 1,
                "zone_id": "string"
              },
              "cluster_log_conf": {
                "dbfs": {},
                "s3": {},
                "volumes": {}
              },
              "cluster_name": "Ava Chen",
              "custom_tags": {},
              "data_security_mode": "string",
              "docker_image": {
                "basic_auth": {},
                "url": "https://example.com"
              },
              "driver_instance_pool_id": "string",
              "driver_node_type_flexibility": {
                "alternate_node_type_ids": [
                  "string"
                ]
              },
              "driver_node_type_id": "string",
              "enable_elastic_disk": true,
              "enable_local_disk_encryption": true,
              "init_scripts": [
                {
                  "abfss": {},
                  "dbfs": {},
                  "file": {},
                  "gcs": {},
                  "s3": {},
                  "volumes": {},
                  "workspace": {}
                }
              ],
              "instance_pool_id": "string",
              "is_single_node": true,
              "kind": "string",
              "node_type_id": "string",
              "num_workers": 1,
              "policy_id": "string",
              "runtime_engine": "string",
              "single_user_name": "Ava Chen",
              "spark_conf": {},
              "spark_env_vars": {},
              "spark_version": "string",
              "ssh_public_keys": [
                "string"
              ],
              "use_ml_runtime": true,
              "worker_node_type_flexibility": {
                "alternate_node_type_ids": [
                  "string"
                ]
              },
              "workload_type": {
                "clients": {}
              }
            }
          }
        ],
        "max_concurrent_runs": 1,
        "name": "Ava Chen",
        "notification_settings": {
          "no_alert_for_canceled_runs": true,
          "no_alert_for_skipped_runs": true
        },
        "parameters": [
          {
            "default": "string",
            "name": "Ava Chen"
          }
        ],
        "performance_target": "string",
        "queue": {
          "enabled": true
        },
        "run_as": {
          "service_principal_name": "Ava Chen",
          "user_name": "Ava Chen"
        },
        "schedule": {
          "pause_status": "string",
          "quartz_cron_expression": "string",
          "timezone_id": "string"
        },
        "tags": {},
        "tasks": [
          {
            "alert_task": {
              "alert_id": "string",
              "subscribers": [
                {
                  "destination_id": "string",
                  "user_name": "Ava Chen"
                }
              ],
              "warehouse_id": "string",
              "workspace_path": "string"
            },
            "clean_rooms_notebook_task": {
              "clean_room_name": "Ava Chen",
              "etag": "string",
              "notebook_base_parameters": {},
              "notebook_name": "Ava Chen"
            },
            "compute": {
              "hardware_accelerator": "string"
            },
            "condition_task": {
              "left": "string",
              "op": "string",
              "right": "string"
            },
            "dashboard_task": {
              "dashboard_id": "string",
              "subscription": {
                "custom_subject": "string",
                "paused": true,
                "subscribers": [
                  "string"
                ]
              },
              "warehouse_id": "string"
            },
            "dbt_task": {
              "catalog": "string",
              "commands": [
                "string"
              ],
              "profiles_directory": "string",
              "project_directory": "string",
              "schema": "string",
              "source": "string",
              "warehouse_id": "string"
            },
            "depends_on": [
              {
                "outcome": "string",
                "task_key": "string"
              }
            ],
            "description": "string",
            "disable_auto_optimization": true,
            "email_notifications": {
              "no_alert_for_skipped_runs": true,
              "on_duration_warning_threshold_exceeded": [
                "ava@example.com"
              ],
              "on_failure": [
                "ava@example.com"
              ],
              "on_start": [
                "ava@example.com"
              ],
              "on_streaming_backlog_exceeded": [
                "ava@example.com"
              ],
              "on_success": [
                "ava@example.com"
              ]
            },
            "environment_key": "string",
            "existing_cluster_id": "string",
            "for_each_task": {
              "concurrency": 1,
              "inputs": "string",
              "task": {
                "alert_task": {},
                "clean_rooms_notebook_task": {},
                "compute": {},
                "condition_task": {},
                "dashboard_task": {},
                "dbt_task": {},
                "depends_on": [
                  "string"
                ],
                "description": "string",
                "disable_auto_optimization": true,
                "email_notifications": {},
                "environment_key": "string",
                "existing_cluster_id": "string",
                "for_each_task": {},
                "health": {},
                "job_cluster_key": "string",
                "libraries": [
                  "string"
                ],
                "max_retries": 1,
                "min_retry_interval_millis": 1,
                "new_cluster": {},
                "notebook_task": {},
                "notification_settings": {},
                "pipeline_task": {},
                "power_bi_task": {},
                "python_wheel_task": {},
                "retry_on_timeout": true,
                "run_if": "string",
                "run_job_task": {},
                "spark_jar_task": {},
                "spark_python_task": {},
                "spark_submit_task": {},
                "sql_task": {},
                "task_key": "string",
                "timeout_seconds": 1,
                "webhook_notifications": {}
              }
            },
            "health": {
              "rules": [
                {
                  "metric": "string",
                  "op": "string",
                  "value": 1
                }
              ]
            },
            "job_cluster_key": "string",
            "libraries": [
              {
                "cran": {
                  "package": "string",
                  "repo": "string"
                },
                "egg": "string",
                "jar": "string",
                "maven": {
                  "coordinates": "string",
                  "exclusions": [
                    "string"
                  ],
                  "repo": "string"
                },
                "pypi": {
                  "package": "string",
                  "repo": "string"
                },
                "requirements": "string",
                "whl": "string"
              }
            ],
            "max_retries": 1,
            "min_retry_interval_millis": 1,
            "new_cluster": {
              "apply_policy_default_values": true,
              "autoscale": {
                "max_workers": 1,
                "min_workers": 1
              },
              "autotermination_minutes": 1,
              "aws_attributes": {
                "availability": "string",
                "ebs_volume_count": 1,
                "ebs_volume_iops": 1,
                "ebs_volume_size": 1,
                "ebs_volume_throughput": 1,
                "ebs_volume_type": "string",
                "first_on_demand": 1,
                "instance_profile_arn": "string",
                "spot_bid_price_percent": 1,
                "zone_id": "string"
              },
              "cluster_log_conf": {
                "dbfs": {},
                "s3": {},
                "volumes": {}
              },
              "cluster_name": "Ava Chen",
              "custom_tags": {},
              "data_security_mode": "string",
              "docker_image": {
                "basic_auth": {},
                "url": "https://example.com"
              },
              "driver_instance_pool_id": "string",
              "driver_node_type_flexibility": {
                "alternate_node_type_ids": [
                  "string"
                ]
              },
              "driver_node_type_id": "string",
              "enable_elastic_disk": true,
              "enable_local_disk_encryption": true,
              "init_scripts": [
                {
                  "abfss": {},
                  "dbfs": {},
                  "file": {},
                  "gcs": {},
                  "s3": {},
                  "volumes": {},
                  "workspace": {}
                }
              ],
              "instance_pool_id": "string",
              "is_single_node": true,
              "kind": "string",
              "node_type_id": "string",
              "num_workers": 1,
              "policy_id": "string",
              "runtime_engine": "string",
              "single_user_name": "Ava Chen",
              "spark_conf": {},
              "spark_env_vars": {},
              "spark_version": "string",
              "ssh_public_keys": [
                "string"
              ],
              "use_ml_runtime": true,
              "worker_node_type_flexibility": {
                "alternate_node_type_ids": [
                  "string"
                ]
              },
              "workload_type": {
                "clients": {}
              }
            },
            "notebook_task": {
              "base_parameters": {},
              "notebook_path": "string",
              "source": "string",
              "warehouse_id": "string"
            },
            "notification_settings": {
              "alert_on_last_attempt": true,
              "no_alert_for_canceled_runs": true,
              "no_alert_for_skipped_runs": true
            },
            "pipeline_task": {
              "full_refresh": true,
              "pipeline_id": "string"
            },
            "power_bi_task": {
              "connection_resource_name": "Ava Chen",
              "power_bi_model": {
                "authentication_method": "string",
                "model_name": "Ava Chen",
                "overwrite_existing": true,
                "storage_mode": "string",
                "workspace_name": "Ava Chen"
              },
              "refresh_after_update": true,
              "tables": [
                {
                  "catalog": "string",
                  "name": "Ava Chen",
                  "schema": "string",
                  "storage_mode": "string"
                }
              ],
              "warehouse_id": "string"
            },
            "python_wheel_task": {
              "entry_point": "string",
              "named_parameters": {},
              "package_name": "Ava Chen",
              "parameters": [
                "string"
              ]
            },
            "retry_on_timeout": true,
            "run_if": "string",
            "run_job_task": {
              "job_id": 1,
              "job_parameters": {},
              "pipeline_params": {
                "full_refresh": true
              }
            },
            "spark_jar_task": {
              "jar_uri": "string",
              "main_class_name": "Ava Chen",
              "parameters": [
                "string"
              ],
              "run_as_repl": true
            },
            "spark_python_task": {
              "parameters": [
                "string"
              ],
              "python_file": "string",
              "source": "string"
            },
            "spark_submit_task": {
              "parameters": [
                "string"
              ]
            },
            "sql_task": {
              "alert": {
                "alert_id": "string",
                "pause_subscriptions": true,
                "subscriptions": [
                  "string"
                ]
              },
              "dashboard": {
                "custom_subject": "string",
                "dashboard_id": "string",
                "pause_subscriptions": true,
                "subscriptions": [
                  "string"
                ]
              },
              "file": {
                "path": "string",
                "source": "string"
              },
              "parameters": {},
              "query": {
                "query_id": "string"
              },
              "warehouse_id": "string"
            },
            "task_key": "string",
            "timeout_seconds": 1,
            "webhook_notifications": {
              "on_duration_warning_threshold_exceeded": [
                {
                  "id": "string"
                }
              ],
              "on_failure": [
                {
                  "id": "string"
                }
              ],
              "on_start": [
                {
                  "id": "string"
                }
              ],
              "on_streaming_backlog_exceeded": [
                {
                  "id": "string"
                }
              ],
              "on_success": [
                {
                  "id": "string"
                }
              ]
            }
          }
        ],
        "timeout_seconds": 1,
        "trigger": {
          "file_arrival": {
            "min_time_between_triggers_seconds": 1,
            "url": "https://example.com",
            "wait_after_last_change_seconds": 1
          },
          "pause_status": "string",
          "periodic": {
            "interval": 1,
            "unit": "string"
          },
          "table_update": {
            "condition": "string",
            "min_time_between_triggers_seconds": 1,
            "table_names": [
              "Ava Chen"
            ],
            "wait_after_last_change_seconds": 1
          }
        },
        "webhook_notifications": {
          "on_duration_warning_threshold_exceeded": [
            {
              "id": "string"
            }
          ],
          "on_failure": [
            {
              "id": "string"
            }
          ],
          "on_start": [
            {
              "id": "string"
            }
          ],
          "on_streaming_backlog_exceeded": [
            {
              "id": "string"
            }
          ],
          "on_success": [
            {
              "id": "string"
            }
          ]
        }
      },
      "trigger_state": {
        "file_arrival": {
          "using_file_events": true
        },
        "table": {
          "last_seen_table_states": [
            {
              "has_seen_updates": true,
              "table_name": "Ava Chen"
            }
          ],
          "using_scalable_monitoring": true
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_time` | number | The time at which this job was created in epoch milliseconds (milliseconds since 1/1/1970 UTC). |
| `creator_user_name` | string | The creator user name. This field wonât be included in the response if the user has already been deleted. |
| `effective_budget_policy_id` | string | The id of the budget policy used by this job for cost attribution purposes. This may be set through (in order of precedence): 1. Budget admins through the account or workspace console 2. Jobs UI in the job details page and Jobs API using `budget_policy_id` 3. Inferred default based on accessible budget policies of the run_as identity on job creation or modification. |
| `has_more` | boolean | Indicates if the job has more array properties (`tasks`, `job_clusters`) that are not shown. They can be accessed via :method:jobs/get endpoint. It is only relevant for API 2.2 :method:jobs/list requests with `expand_tasks=true`. |
| `job_id` | number | The canonical identifier for this job. |
| `settings` | object |  |
| `settings.budget_policy_id` | string | The id of the user specified budget policy to use for this job. If not specified, a default budget policy may be applied when creating or modifying the job. See `effective_budget_policy_id` for the budget policy used by this workload. |
| `settings.continuous` | object |  |
| `settings.continuous.pause_status` | string |  |
| `settings.continuous.task_retry_mode` | string | task retry mode of the continuous job * NEVER: The failed task will not be retried. * ON_FAILURE: Retry a failed task if at least one other task in the job is still running its first attempt. When this condition is no longer met or the retry limit is reached, the job run is cancelled and a new run is started. |
| `settings.deployment` | object |  |
| `settings.deployment.kind` | string | * `BUNDLE`: The job is managed by Databricks Asset Bundle. * `SYSTEM_MANAGED`: The job is managed by Databricks and is read-only. |
| `settings.deployment.metadata_file_path` | string | Path of the file that contains deployment metadata. |
| `settings.description` | string | An optional description for the job. The maximum length is 27700 characters in UTF-8 encoding. |
| `settings.edit_mode` | string | Edit mode of the job.  * `UI_LOCKED`: The job is in a locked UI state and cannot be modified. * `EDITABLE`: The job is in an editable state and can be modified. |
| `settings.email_notifications` | object |  |
| `settings.email_notifications.no_alert_for_skipped_runs` | boolean | If true, do not send email to recipients specified in `on_failure` if the run is skipped. This field is `deprecated`. Please use the `notification_settings.no_alert_for_skipped_runs` field. |
| `settings.email_notifications.on_duration_warning_threshold_exceeded` | array<string> | A list of email addresses to be notified when the duration of a run exceeds the threshold specified for the `RUN_DURATION_SECONDS` metric in the `health` field. If no rule for the `RUN_DURATION_SECONDS` metric is specified in the `health` field for the job, notifications are not sent. |
| `settings.email_notifications.on_failure` | array<string> | A list of email addresses to be notified when a run unsuccessfully completes. A run is considered to have completed unsuccessfully if it ends with an `INTERNAL_ERROR` `life_cycle_state` or a `FAILED`, or `TIMED_OUT` result_state. If this is not specified on job creation, reset, or update the list is empty, and notifications are not sent. |
| `settings.email_notifications.on_start` | array<string> | A list of email addresses to be notified when a run begins. If not specified on job creation, reset, or update, the list is empty, and notifications are not sent. |
| `settings.email_notifications.on_streaming_backlog_exceeded` | array<string> | A list of email addresses to notify when any streaming backlog thresholds are exceeded for any stream. Streaming backlog thresholds can be set in the `health` field using the following metrics: `STREAMING_BACKLOG_BYTES`, `STREAMING_BACKLOG_RECORDS`, `STREAMING_BACKLOG_SECONDS`, or `STREAMING_BACKLOG_FILES`. Alerting is based on the 10-minute average of these metrics. If the issue persists, notifications are resent every 30 minutes. |
| `settings.email_notifications.on_success` | array<string> | A list of email addresses to be notified when a run successfully completes. A run is considered to have completed successfully if it ends with a `TERMINATED` `life_cycle_state` and a `SUCCESS` result_state. If not specified on job creation, reset, or update, the list is empty, and notifications are not sent. |
| `settings.environments` | array<string> | A list of task execution environment specifications that can be referenced by serverless tasks of this job. For serverless notebook tasks, if the environment_key is not specified, the notebook environment will be used if present. If a jobs environment is specified, it will override the notebook environment. For other serverless tasks, the task environment is required to be specified using environment_key in the task settings. |
| `settings.environments[].environment_key` | string | The key of an environment. It has to be unique within a job. |
| `settings.environments[].spec` | object | The environment entity used to preserve serverless environment side panel, jobs' environment for non-notebook task, and DLT's environment for classic and serverless pipelines. In this minimal environment spec, only pip and java dependencies are supported. |
| `settings.environments[].spec.base_environment` | string | The `base_environment` key refers to an `env.yaml` file that specifies an environment version and a collection of dependencies required for the environment setup. This `env.yaml` file may itself include a `base_environment` reference pointing to another `env_1.yaml` file. However, when used as a base environment, `env_1.yaml` (or further nested references) will not be processed or included in the final environment, meaning that the resolution of `base_environment` references is not recursive. |
| `settings.environments[].spec.client` | string | Use `environment_version` instead. |
| `settings.environments[].spec.dependencies` | array<string> | List of pip dependencies, as supported by the version of pip in this environment. Each dependency is a valid pip requirements file line per https://pip.pypa.io/en/stable/reference/requirements-file-format/. Allowed dependencies include a requirement specifier, an archive URL, a local project path (such as WSFS or UC Volumes in Databricks), or a VCS project URL. |
| `settings.environments[].spec.environment_version` | string | Either `environment_version` or `base_environment` needs to be provided. Environment version used by the environment. Each version comes with a specific Python version and a set of Python packages. The version is a string, consisting of an integer. See https://docs.databricks.com/aws/release-notes/serverless/#serverless-environment-versions. |
| `settings.environments[].spec.java_dependencies` | array<string> | List of java dependencies. Each dependency is a string representing a java library path. For example: `/Volumes/path/to/test.jar`. See https://docs.databricks.com/aws/en/jobs/jar. |
| `settings.format` | string |  |
| `settings.git_source` | object | An optional specification for a remote Git repository containing the source code used by tasks. Version-controlled source code is supported by notebook, dbt, Python script, and SQL File tasks.  If `git_source` is set, these tasks retrieve the file from the remote repository by default. However, this behavior can be overridden by setting `source` to `WORKSPACE` on the task.  Note: dbt and SQL File tasks support only version-controlled sources. If dbt or SQL File tasks are used, `git_source` must be defined on the job. |
| `settings.git_source.git_branch` | string | Name of the branch to be checked out and used by this job. This field cannot be specified in conjunction with git_tag or git_commit. |
| `settings.git_source.git_commit` | string | Commit to be checked out and used by this job. This field cannot be specified in conjunction with git_branch or git_tag. |
| `settings.git_source.git_provider` | string |  |
| `settings.git_source.git_snapshot` | object | Read-only state of the remote repository at the time the job was run. This field is only included on job runs. |
| `settings.git_source.git_snapshot.used_commit` | string | Commit that was used to execute the run. If git_branch was specified, this points to the HEAD of the branch at the time of the run; if git_tag was specified, this points to the commit the tag points to. |
| `settings.git_source.git_tag` | string | Name of the tag to be checked out and used by this job. This field cannot be specified in conjunction with git_branch or git_commit. |
| `settings.git_source.git_url` | string | URL of the repository to be cloned by this job. |
| `settings.git_source.sparse_checkout` | object |  |
| `settings.git_source.sparse_checkout.patterns` | array<string> | List of patterns to include for sparse checkout. |
| `settings.health` | object | An optional set of health rules that can be defined for this job. |
| `settings.health.rules` | array<string> |  |
| `settings.health.rules[].metric` | string | Specifies the health metric that is being evaluated for a particular health rule.  * `RUN_DURATION_SECONDS`: Expected total time for a run in seconds. * `STREAMING_BACKLOG_BYTES`: An estimate of the maximum bytes of data waiting to be consumed across all streams. This metric is in Public Preview. * `STREAMING_BACKLOG_RECORDS`: An estimate of the maximum offset lag across all streams. This metric is in Public Preview. * `STREAMING_BACKLOG_SECONDS`: An estimate of the maximum consumer delay across all streams. This metric is in Public Preview. * `STREAMING_BACKLOG_FILES`: An estimate of the maximum number of outstanding files across all streams. This metric is in Public Preview. |
| `settings.health.rules[].op` | string | Specifies the operator used to compare the health metric value with the specified threshold. |
| `settings.health.rules[].value` | number | Specifies the threshold value that the health metric should obey to satisfy the health rule. |
| `settings.job_clusters` | array<string> | A list of job cluster specifications that can be shared and reused by tasks of this job. Libraries cannot be declared in a shared job cluster. You must declare dependent libraries in task settings. |
| `settings.job_clusters[].job_cluster_key` | string | A unique name for the job cluster. This field is required and must be unique within the job. `JobTaskSettings` may refer to this field to determine which cluster to launch for the task execution. |
| `settings.job_clusters[].new_cluster` | object | Contains a snapshot of the latest user specified settings that were used to create/edit the cluster. |
| `settings.job_clusters[].new_cluster.apply_policy_default_values` | boolean | When set to true, fixed and default values from the policy will be used for fields that are omitted. When set to false, only fixed values from the policy will be applied. |
| `settings.job_clusters[].new_cluster.autoscale` | object |  |
| `settings.job_clusters[].new_cluster.autoscale.max_workers` | number | The maximum number of workers to which the cluster can scale up when overloaded. Note that `max_workers` must be strictly greater than `min_workers`. |
| `settings.job_clusters[].new_cluster.autoscale.min_workers` | number | The minimum number of workers to which the cluster can scale down when underutilized. It is also the initial number of workers the cluster will have after creation. |
| `settings.job_clusters[].new_cluster.autotermination_minutes` | number | Automatically terminates the cluster after it is inactive for this time in minutes. If not set, this cluster will not be automatically terminated. If specified, the threshold must be between 10 and 10000 minutes. Users can also set this value to 0 to explicitly disable automatic termination. |
| `settings.job_clusters[].new_cluster.aws_attributes` | object | Attributes set during cluster creation which are related to Amazon Web Services. |
| `settings.job_clusters[].new_cluster.aws_attributes.availability` | string | Availability type used for all subsequent nodes past the `first_on_demand` ones.  Note: If `first_on_demand` is zero, this availability type will be used for the entire cluster. |
| `settings.job_clusters[].new_cluster.aws_attributes.ebs_volume_count` | number | The number of volumes launched for each instance. Users can choose up to 10 volumes. This feature is only enabled for supported node types. Legacy node types cannot specify custom EBS volumes. For node types with no instance store, at least one EBS volume needs to be specified; otherwise, cluster creation will fail.  These EBS volumes will be mounted at `/ebs0`, `/ebs1`, and etc. Instance store volumes will be mounted at `/local_disk0`, `/local_disk1`, and etc.  If EBS volumes are attached, Databricks will configure Spark to use only the EBS volumes for scratch storage because heterogenously sized scratch devices can lead to inefficient disk utilization. If no EBS volumes are attached, Databricks will configure Spark to use instance store volumes.  Please note that if EBS volumes are specified, then the Spark configuration `spark.local.dir` will be overridden. |
| `settings.job_clusters[].new_cluster.aws_attributes.ebs_volume_iops` | number | If using gp3 volumes, what IOPS to use for the disk. If this is not set, the maximum performance of a gp2 volume with the same volume size will be used. |
| `settings.job_clusters[].new_cluster.aws_attributes.ebs_volume_size` | number | The size of each EBS volume (in GiB) launched for each instance. For general purpose SSD, this value must be within the range 100 - 4096. For throughput optimized HDD, this value must be within the range 500 - 4096. |
| `settings.job_clusters[].new_cluster.aws_attributes.ebs_volume_throughput` | number | If using gp3 volumes, what throughput to use for the disk. If this is not set, the maximum performance of a gp2 volume with the same volume size will be used. |
| `settings.job_clusters[].new_cluster.aws_attributes.ebs_volume_type` | string | All EBS volume types that Databricks supports. See https://aws.amazon.com/ebs/details/ for details. |
| `settings.job_clusters[].new_cluster.aws_attributes.first_on_demand` | number | The first `first_on_demand` nodes of the cluster will be placed on on-demand instances. If this value is greater than 0, the cluster driver node in particular will be placed on an on-demand instance. If this value is greater than or equal to the current cluster size, all nodes will be placed on on-demand instances. If this value is less than the current cluster size, `first_on_demand` nodes will be placed on on-demand instances and the remainder will be placed on `availability` instances. Note that this value does not affect cluster size and cannot currently be mutated over the lifetime of a cluster. |
| `settings.job_clusters[].new_cluster.aws_attributes.instance_profile_arn` | string | Nodes for this cluster will only be placed on AWS instances with this instance profile. If ommitted, nodes will be placed on instances without an IAM instance profile. The instance profile must have previously been added to the Databricks environment by an account administrator.  This feature may only be available to certain customer plans. |
| `settings.job_clusters[].new_cluster.aws_attributes.spot_bid_price_percent` | number | The bid price for AWS spot instances, as a percentage of the corresponding instance type's on-demand price. For example, if this field is set to 50, and the cluster needs a new `r3.xlarge` spot instance, then the bid price is half of the price of on-demand `r3.xlarge` instances. Similarly, if this field is set to 200, the bid price is twice the price of on-demand `r3.xlarge` instances. If not specified, the default value is 100. When spot instances are requested for this cluster, only spot instances whose bid price percentage matches this field will be considered. Note that, for safety, we enforce this field to be no more than 10000. |
| `settings.job_clusters[].new_cluster.aws_attributes.zone_id` | string | Identifier for the availability zone/datacenter in which the cluster resides. This string will be of a form like "us-west-2a". The provided availability zone must be in the same region as the Databricks deployment. For example, "us-west-2a" is not a valid zone id if the Databricks deployment resides in the "us-east-1" region. This is an optional field at cluster creation, and if not specified, the zone "auto" will be used. If the zone specified is "auto", will try to place cluster in a zone with high availability, and will retry placement in a different AZ if there is not enough capacity.  The list of available zones as well as the default value can be found by using the `List Zones` method. |
| `settings.job_clusters[].new_cluster.cluster_log_conf` | object | Cluster log delivery config |
| `settings.job_clusters[].new_cluster.cluster_log_conf.dbfs` | object | A storage location in DBFS |
| `settings.job_clusters[].new_cluster.cluster_log_conf.s3` | object | A storage location in Amazon S3 |
| `settings.job_clusters[].new_cluster.cluster_log_conf.volumes` | object | A storage location back by UC Volumes. |
| `settings.job_clusters[].new_cluster.cluster_name` | string | Cluster name requested by the user. This doesn't have to be unique. If not specified at creation, the cluster name will be an empty string. For job clusters, the cluster name is automatically set based on the job and job run IDs. |
| `settings.job_clusters[].new_cluster.custom_tags` | object | Additional tags for cluster resources. Databricks will tag all cluster resources (e.g., AWS instances and EBS volumes) with these tags in addition to `default_tags`. Notes:  - Currently, Databricks allows at most 45 custom tags  - Clusters can only reuse cloud resources if the resources' tags are a subset of the cluster tags |
| `settings.job_clusters[].new_cluster.data_security_mode` | string | Data security mode decides what data governance model to use when accessing data from a cluster.  The following modes can only be used when `kind = CLASSIC_PREVIEW`. * `DATA_SECURITY_MODE_AUTO`: Databricks will choose the most appropriate access mode depending on your compute configuration. * `DATA_SECURITY_MODE_STANDARD`: Alias for `USER_ISOLATION`. * `DATA_SECURITY_MODE_DEDICATED`: Alias for `SINGLE_USER`.  The following modes can be used regardless of `kind`. * `NONE`: No security isolation for multiple users sharing the cluster. Data governance features are not available in this mode. * `SINGLE_USER`: A secure cluster that can only be exclusively used by a single user specified in `single_user_name`. Most programming languages, cluster features and data governance features are available in this mode. * `USER_ISOLATION`: A secure cluster that can be shared by multiple users. Cluster users are fully isolated so that they cannot see each other's data and credentials. Most data governance features are supported in this mode. But programming languages and cluster features might be limited.  The following modes are deprecated starting with Databricks Runtime 15.0 and will be removed for future Databricks Runtime versions:  * `LEGACY_TABLE_ACL`: This mode is for users migrating from legacy Table ACL clusters. * `LEGACY_PASSTHROUGH`: This mode is for users migrating from legacy Passthrough on high concurrency clusters. * `LEGACY_SINGLE_USER`: This mode is for users migrating from legacy Passthrough on standard clusters. * `LEGACY_SINGLE_USER_STANDARD`: This mode provides a way that doesnât have UC nor passthrough enabled. |
| `settings.job_clusters[].new_cluster.docker_image` | object |  |
| `settings.job_clusters[].new_cluster.docker_image.basic_auth` | object |  |
| `settings.job_clusters[].new_cluster.docker_image.url` | string | URL of the docker image. |
| `settings.job_clusters[].new_cluster.driver_instance_pool_id` | string | The optional ID of the instance pool for the driver of the cluster belongs. The pool cluster uses the instance pool with id (instance_pool_id) if the driver pool is not assigned. |
| `settings.job_clusters[].new_cluster.driver_node_type_flexibility` | object | Configuration for flexible node types, allowing fallback to alternate node types during cluster launch and upscale. |
| `settings.job_clusters[].new_cluster.driver_node_type_flexibility.alternate_node_type_ids` | array<string> | A list of node type IDs to use as fallbacks when the primary node type is unavailable. |
| `settings.job_clusters[].new_cluster.driver_node_type_id` | string | The node type of the Spark driver. Note that this field is optional; if unset, the driver node type will be set as the same value as `node_type_id` defined above.  This field, along with node_type_id, should not be set if virtual_cluster_size is set. If both driver_node_type_id, node_type_id, and virtual_cluster_size are specified, driver_node_type_id and node_type_id take precedence. |
| `settings.job_clusters[].new_cluster.enable_elastic_disk` | boolean | Autoscaling Local Storage: when enabled, this cluster will dynamically acquire additional disk space when its Spark workers are running low on disk space.  This feature requires specific AWS permissions to function correctly - refer to the User Guide for more details. |
| `settings.job_clusters[].new_cluster.enable_local_disk_encryption` | boolean | Whether to enable LUKS on cluster VMs' local disks |
| `settings.job_clusters[].new_cluster.init_scripts` | array<string> | The configuration for storing init scripts. Any number of destinations can be specified. The scripts are executed sequentially in the order provided. If `cluster_log_conf` is specified, init script logs are sent to `<destination>/<cluster-ID>/init_scripts`. |
| `settings.job_clusters[].new_cluster.init_scripts[].abfss` | object | A storage location in Adls Gen2 |
| `settings.job_clusters[].new_cluster.init_scripts[].dbfs` | object | A storage location in DBFS |
| `settings.job_clusters[].new_cluster.init_scripts[].file` | object |  |
| `settings.job_clusters[].new_cluster.init_scripts[].gcs` | object | A storage location in Google Cloud Platform's GCS |
| `settings.job_clusters[].new_cluster.init_scripts[].s3` | object | A storage location in Amazon S3 |
| `settings.job_clusters[].new_cluster.init_scripts[].volumes` | object | A storage location back by UC Volumes. |
| `settings.job_clusters[].new_cluster.init_scripts[].workspace` | object | A storage location in Workspace Filesystem (WSFS) |
| `settings.job_clusters[].new_cluster.instance_pool_id` | string | The optional ID of the instance pool to which the cluster belongs. |
| `settings.job_clusters[].new_cluster.is_single_node` | boolean | This field can only be used when `kind = CLASSIC_PREVIEW`.  When set to true, Databricks will automatically set single node related `custom_tags`, `spark_conf`, and `num_workers` |
| `settings.job_clusters[].new_cluster.kind` | string | The kind of compute described by this compute specification.  Depending on `kind`, different validations and default values will be applied.  Clusters with `kind = CLASSIC_PREVIEW` support the following fields, whereas clusters with no specified `kind` do not. * [is_single_node](/api/workspace/clusters/create#is_single_node) * [use_ml_runtime](/api/workspace/clusters/create#use_ml_runtime) * [data_security_mode](/api/workspace/clusters/create#data_security_mode) set to `DATA_SECURITY_MODE_AUTO`, `DATA_SECURITY_MODE_DEDICATED`, or `DATA_SECURITY_MODE_STANDARD`  By using the [simple form](https://docs.databricks.com/compute/simple-form.html), your clusters are automatically using `kind = CLASSIC_PREVIEW`. |
| `settings.job_clusters[].new_cluster.node_type_id` | string | This field encodes, through a single value, the resources available to each of the Spark nodes in this cluster. For example, the Spark nodes can be provisioned and optimized for memory or compute intensive workloads. A list of available node types can be retrieved by using the :method:clusters/listNodeTypes API call. |
| `settings.job_clusters[].new_cluster.num_workers` | number | Number of worker nodes that this cluster should have. A cluster has one Spark Driver and `num_workers` Executors for a total of `num_workers` + 1 Spark nodes.  Note: When reading the properties of a cluster, this field reflects the desired number of workers rather than the actual current number of workers. For instance, if a cluster is resized from 5 to 10 workers, this field will immediately be updated to reflect the target size of 10 workers, whereas the workers listed in `spark_info` will gradually increase from 5 to 10 as the new nodes are provisioned. |
| `settings.job_clusters[].new_cluster.policy_id` | string | The ID of the cluster policy used to create the cluster if applicable. |
| `settings.job_clusters[].new_cluster.runtime_engine` | string |  |
| `settings.job_clusters[].new_cluster.single_user_name` | string | Single user name if data_security_mode is `SINGLE_USER` |
| `settings.job_clusters[].new_cluster.spark_conf` | object | An object containing a set of optional, user-specified Spark configuration key-value pairs. Users can also pass in a string of extra JVM options to the driver and the executors via `spark.driver.extraJavaOptions` and `spark.executor.extraJavaOptions` respectively. |
| `settings.job_clusters[].new_cluster.spark_env_vars` | object | An object containing a set of optional, user-specified environment variable key-value pairs. Please note that key-value pair of the form (X,Y) will be exported as is (i.e., `export X='Y'`) while launching the driver and workers.  In order to specify an additional set of `SPARK_DAEMON_JAVA_OPTS`, we recommend appending them to `$SPARK_DAEMON_JAVA_OPTS` as shown in the example below. This ensures that all default databricks managed environmental variables are included as well.  Example Spark environment variables: `{"SPARK_WORKER_MEMORY": "28000m", "SPARK_LOCAL_DIRS": "/local_disk0"}` or `{"SPARK_DAEMON_JAVA_OPTS": "$SPARK_DAEMON_JAVA_OPTS -Dspark.shuffle.service.enabled=true"}` |
| `settings.job_clusters[].new_cluster.spark_version` | string | The Spark version of the cluster, e.g. `3.3.x-scala2.11`. A list of available Spark versions can be retrieved by using the :method:clusters/sparkVersions API call. |
| `settings.job_clusters[].new_cluster.ssh_public_keys` | array<string> | SSH public key contents that will be added to each Spark node in this cluster. The corresponding private keys can be used to login with the user name `ubuntu` on port `2200`. Up to 10 keys can be specified. |
| `settings.job_clusters[].new_cluster.use_ml_runtime` | boolean | This field can only be used when `kind = CLASSIC_PREVIEW`.  `effective_spark_version` is determined by `spark_version` (DBR release), this field `use_ml_runtime`, and whether `node_type_id` is gpu node or not. |
| `settings.job_clusters[].new_cluster.worker_node_type_flexibility` | object | Configuration for flexible node types, allowing fallback to alternate node types during cluster launch and upscale. |
| `settings.job_clusters[].new_cluster.worker_node_type_flexibility.alternate_node_type_ids` | array<string> | A list of node type IDs to use as fallbacks when the primary node type is unavailable. |
| `settings.job_clusters[].new_cluster.workload_type` | object | Cluster Attributes showing for clusters workload types. |
| `settings.job_clusters[].new_cluster.workload_type.clients` | object |  |
| `settings.max_concurrent_runs` | number | An optional maximum allowed number of concurrent runs of the job. Set this value if you want to be able to execute multiple runs of the same job concurrently. This is useful for example if you trigger your job on a frequent schedule and want to allow consecutive runs to overlap with each other, or if you want to trigger multiple runs which differ by their input parameters. This setting affects only new runs. For example, suppose the jobâs concurrency is 4 and there are 4 concurrent active runs. Then setting the concurrency to 3 wonât kill any of the active runs. However, from then on, new runs are skipped unless there are fewer than 3 active runs. This value cannot exceed 1000. Setting this value to `0` causes all new runs to be skipped. |
| `settings.name` | string | An optional name for the job. The maximum length is 4096 bytes in UTF-8 encoding. |
| `settings.notification_settings` | object |  |
| `settings.notification_settings.no_alert_for_canceled_runs` | boolean | If true, do not send notifications to recipients specified in `on_failure` if the run is canceled. |
| `settings.notification_settings.no_alert_for_skipped_runs` | boolean | If true, do not send notifications to recipients specified in `on_failure` if the run is skipped. |
| `settings.parameters` | array<string> | Job-level parameter definitions |
| `settings.parameters[].default` | string | Default value of the parameter. |
| `settings.parameters[].name` | string | The name of the defined parameter. May only contain alphanumeric characters, `_`, `-`, and `.` |
| `settings.performance_target` | string | PerformanceTarget defines how performant (lower latency) or cost efficient the execution of run on serverless compute should be. The performance mode on the job or pipeline should map to a performance setting that is passed to Cluster Manager (see cluster-common PerformanceTarget). |
| `settings.queue` | object |  |
| `settings.queue.enabled` | boolean | If true, enable queueing for the job. This is a required field. |
| `settings.run_as` | object | Write-only setting. Specifies the user or service principal that the job runs as. If not specified, the job runs as the user who created the job.  Either `user_name` or `service_principal_name` should be specified. If not, an error is thrown. |
| `settings.run_as.service_principal_name` | string | Application ID of an active service principal. Setting this field requires the `servicePrincipal/user` role. |
| `settings.run_as.user_name` | string | The email of an active workspace user. Non-admin users can only set this field to their own email. |
| `settings.schedule` | object |  |
| `settings.schedule.pause_status` | string |  |
| `settings.schedule.quartz_cron_expression` | string | A Cron expression using Quartz syntax that describes the schedule for a job. See [Cron Trigger](http://www.quartz-scheduler.org/documentation/quartz-2.3.0/tutorials/crontrigger.html) for details. This field is required. |
| `settings.schedule.timezone_id` | string | A Java timezone ID. The schedule for a job is resolved with respect to this timezone. See [Java TimeZone](https://docs.oracle.com/javase/7/docs/api/java/util/TimeZone.html) for details. This field is required. |
| `settings.tags` | object | A map of tags associated with the job. These are forwarded to the cluster as cluster tags for jobs clusters, and are subject to the same limitations as cluster tags. A maximum of 25 tags can be added to the job. |
| `settings.tasks` | array<string> | A list of task specifications to be executed by this job. It supports up to 1000 elements in write endpoints (:method:jobs/create, :method:jobs/reset, :method:jobs/update, :method:jobs/submit). Read endpoints return only 100 tasks. If more than 100 tasks are available, you can paginate through them using :method:jobs/get. Use the `next_page_token` field at the object root to determine if more results are available. |
| `settings.tasks[].alert_task` | object |  |
| `settings.tasks[].alert_task.alert_id` | string | The alert_id is the canonical identifier of the alert. |
| `settings.tasks[].alert_task.subscribers` | array<string> | The subscribers receive alert evaluation result notifications after the alert task is completed. The number of subscriptions is limited to 100. |
| `settings.tasks[].alert_task.subscribers[].destination_id` | string |  |
| `settings.tasks[].alert_task.subscribers[].user_name` | string | A valid workspace email address. |
| `settings.tasks[].alert_task.warehouse_id` | string | The warehouse_id identifies the warehouse settings used by the alert task. |
| `settings.tasks[].alert_task.workspace_path` | string | The workspace_path is the path to the alert file in the workspace. The path: * must start with "/Workspace" * must be a normalized path. User has to select only one of alert_id or workspace_path to identify the alert. |
| `settings.tasks[].clean_rooms_notebook_task` | object | Clean Rooms notebook task for V1 Clean Room service (GA). Replaces the deprecated CleanRoomNotebookTask (defined above) which was for V0 service. |
| `settings.tasks[].clean_rooms_notebook_task.clean_room_name` | string | The clean room that the notebook belongs to. |
| `settings.tasks[].clean_rooms_notebook_task.etag` | string | Checksum to validate the freshness of the notebook resource (i.e. the notebook being run is the latest version). It can be fetched by calling the :method:cleanroomassets/get API. |
| `settings.tasks[].clean_rooms_notebook_task.notebook_base_parameters` | object | Base parameters to be used for the clean room notebook job. |
| `settings.tasks[].clean_rooms_notebook_task.notebook_name` | string | Name of the notebook being run. |
| `settings.tasks[].compute` | object |  |
| `settings.tasks[].compute.hardware_accelerator` | string | HardwareAcceleratorType: The type of hardware accelerator to use for compute workloads. NOTE: This enum is referenced and is intended to be used by other Databricks services that need to specify hardware accelerator requirements for AI compute workloads. |
| `settings.tasks[].condition_task` | object |  |
| `settings.tasks[].condition_task.left` | string | The left operand of the condition task. Can be either a string value or a job state or parameter reference. |
| `settings.tasks[].condition_task.op` | string | * `EQUAL_TO`, `NOT_EQUAL` operators perform string comparison of their operands. This means that `â12.0â == â12â` will evaluate to `false`. * `GREATER_THAN`, `GREATER_THAN_OR_EQUAL`, `LESS_THAN`, `LESS_THAN_OR_EQUAL` operators perform numeric comparison of their operands. `â12.0â >= â12â` will evaluate to `true`, `â10.0â >= â12â` will evaluate to `false`.  The boolean comparison to task values can be implemented with operators `EQUAL_TO`, `NOT_EQUAL`. If a task value was set to a boolean value, it will be serialized to `âtrueâ` or `âfalseâ` for the comparison. |
| `settings.tasks[].condition_task.right` | string | The right operand of the condition task. Can be either a string value or a job state or parameter reference. |
| `settings.tasks[].dashboard_task` | object | Configures the Lakeview Dashboard job task type. |
| `settings.tasks[].dashboard_task.dashboard_id` | string | The identifier of the dashboard to refresh. |
| `settings.tasks[].dashboard_task.subscription` | object |  |
| `settings.tasks[].dashboard_task.subscription.custom_subject` | string | Optional: Allows users to specify a custom subject line on the email sent to subscribers. |
| `settings.tasks[].dashboard_task.subscription.paused` | boolean | When true, the subscription will not send emails. |
| `settings.tasks[].dashboard_task.subscription.subscribers` | array<string> | The list of subscribers to send the snapshot of the dashboard to. |
| `settings.tasks[].dashboard_task.warehouse_id` | string | Optional: The warehouse id to execute the dashboard with for the schedule. If not specified, the default warehouse of the dashboard will be used. |
| `settings.tasks[].dbt_task` | object |  |
| `settings.tasks[].dbt_task.catalog` | string | Optional name of the catalog to use. The value is the top level in the 3-level namespace of Unity Catalog (catalog / schema / relation). The catalog value can only be specified if a warehouse_id is specified. Requires dbt-databricks >= 1.1.1. |
| `settings.tasks[].dbt_task.commands` | array<string> | A list of dbt commands to execute. All commands must start with `dbt`. This parameter must not be empty. A maximum of up to 10 commands can be provided. |
| `settings.tasks[].dbt_task.profiles_directory` | string | Optional (relative) path to the profiles directory. Can only be specified if no warehouse_id is specified. If no warehouse_id is specified and this folder is unset, the root directory is used. |
| `settings.tasks[].dbt_task.project_directory` | string | Path to the project directory. Optional for Git sourced tasks, in which case if no value is provided, the root of the Git repository is used. |
| `settings.tasks[].dbt_task.schema` | string | Optional schema to write to. This parameter is only used when a warehouse_id is also provided. If not provided, the `default` schema is used. |
| `settings.tasks[].dbt_task.source` | string | Optional location type of the SQL file. When set to `WORKSPACE`, the SQL file will be retrieved\ from the local Databricks workspace. When set to `GIT`, the SQL file will be retrieved from a Git repository defined in `git_source`. If the value is empty, the task will use `GIT` if `git_source` is defined and `WORKSPACE` otherwise.  * `WORKSPACE`: SQL file is located in Databricks workspace. * `GIT`: SQL file is located in cloud Git provider. |
| `settings.tasks[].dbt_task.warehouse_id` | string | ID of the SQL warehouse to connect to. If provided, we automatically generate and provide the profile and connection details to dbt. It can be overridden on a per-command basis by using the `--profiles-dir` command line argument. |
| `settings.tasks[].depends_on` | array<string> | An optional array of objects specifying the dependency graph of the task. All tasks specified in this field must complete before executing this task. The task will run only if the `run_if` condition is true. The key is `task_key`, and the value is the name assigned to the dependent task. |
| `settings.tasks[].depends_on[].outcome` | string | Can only be specified on condition task dependencies. The outcome of the dependent task that must be met for this task to run. |
| `settings.tasks[].depends_on[].task_key` | string | The name of the task this task depends on. |
| `settings.tasks[].description` | string | An optional description for this task. |
| `settings.tasks[].disable_auto_optimization` | boolean | An option to disable auto optimization in serverless |
| `settings.tasks[].email_notifications` | object |  |
| `settings.tasks[].email_notifications.no_alert_for_skipped_runs` | boolean | If true, do not send email to recipients specified in `on_failure` if the run is skipped. This field is `deprecated`. Please use the `notification_settings.no_alert_for_skipped_runs` field. |
| `settings.tasks[].email_notifications.on_duration_warning_threshold_exceeded` | array<string> | A list of email addresses to be notified when the duration of a run exceeds the threshold specified for the `RUN_DURATION_SECONDS` metric in the `health` field. If no rule for the `RUN_DURATION_SECONDS` metric is specified in the `health` field for the job, notifications are not sent. |
| `settings.tasks[].email_notifications.on_failure` | array<string> | A list of email addresses to be notified when a run unsuccessfully completes. A run is considered to have completed unsuccessfully if it ends with an `INTERNAL_ERROR` `life_cycle_state` or a `FAILED`, or `TIMED_OUT` result_state. If this is not specified on job creation, reset, or update the list is empty, and notifications are not sent. |
| `settings.tasks[].email_notifications.on_start` | array<string> | A list of email addresses to be notified when a run begins. If not specified on job creation, reset, or update, the list is empty, and notifications are not sent. |
| `settings.tasks[].email_notifications.on_streaming_backlog_exceeded` | array<string> | A list of email addresses to notify when any streaming backlog thresholds are exceeded for any stream. Streaming backlog thresholds can be set in the `health` field using the following metrics: `STREAMING_BACKLOG_BYTES`, `STREAMING_BACKLOG_RECORDS`, `STREAMING_BACKLOG_SECONDS`, or `STREAMING_BACKLOG_FILES`. Alerting is based on the 10-minute average of these metrics. If the issue persists, notifications are resent every 30 minutes. |
| `settings.tasks[].email_notifications.on_success` | array<string> | A list of email addresses to be notified when a run successfully completes. A run is considered to have completed successfully if it ends with a `TERMINATED` `life_cycle_state` and a `SUCCESS` result_state. If not specified on job creation, reset, or update, the list is empty, and notifications are not sent. |
| `settings.tasks[].environment_key` | string | The key that references an environment spec in a job. This field is required for Python script, Python wheel and dbt tasks when using serverless compute. |
| `settings.tasks[].existing_cluster_id` | string | If existing_cluster_id, the ID of an existing cluster that is used for all runs. When running jobs or tasks on an existing cluster, you may need to manually restart the cluster if it stops responding. We suggest running jobs and tasks on new clusters for greater reliability |
| `settings.tasks[].for_each_task` | object |  |
| `settings.tasks[].for_each_task.concurrency` | number | An optional maximum allowed number of concurrent runs of the task. Set this value if you want to be able to execute multiple runs of the task concurrently. |
| `settings.tasks[].for_each_task.inputs` | string | Array for task to iterate on. This can be a JSON string or a reference to an array parameter. |
| `settings.tasks[].for_each_task.task` | object |  |
| `settings.tasks[].for_each_task.task.alert_task` | object |  |
| `settings.tasks[].for_each_task.task.clean_rooms_notebook_task` | object | Clean Rooms notebook task for V1 Clean Room service (GA). Replaces the deprecated CleanRoomNotebookTask (defined above) which was for V0 service. |
| `settings.tasks[].for_each_task.task.compute` | object |  |
| `settings.tasks[].for_each_task.task.condition_task` | object |  |
| `settings.tasks[].for_each_task.task.dashboard_task` | object | Configures the Lakeview Dashboard job task type. |
| `settings.tasks[].for_each_task.task.dbt_task` | object |  |
| `settings.tasks[].for_each_task.task.depends_on` | array<string> | An optional array of objects specifying the dependency graph of the task. All tasks specified in this field must complete before executing this task. The task will run only if the `run_if` condition is true. The key is `task_key`, and the value is the name assigned to the dependent task. |
| `settings.tasks[].for_each_task.task.description` | string | An optional description for this task. |
| `settings.tasks[].for_each_task.task.disable_auto_optimization` | boolean | An option to disable auto optimization in serverless |
| `settings.tasks[].for_each_task.task.email_notifications` | object |  |
| `settings.tasks[].for_each_task.task.environment_key` | string | The key that references an environment spec in a job. This field is required for Python script, Python wheel and dbt tasks when using serverless compute. |
| `settings.tasks[].for_each_task.task.existing_cluster_id` | string | If existing_cluster_id, the ID of an existing cluster that is used for all runs. When running jobs or tasks on an existing cluster, you may need to manually restart the cluster if it stops responding. We suggest running jobs and tasks on new clusters for greater reliability |
| `settings.tasks[].for_each_task.task.for_each_task` | object |  |
| `settings.tasks[].for_each_task.task.health` | object | An optional set of health rules that can be defined for this job. |
| `settings.tasks[].for_each_task.task.job_cluster_key` | string | If job_cluster_key, this task is executed reusing the cluster specified in `job.settings.job_clusters`. |
| `settings.tasks[].for_each_task.task.libraries` | array<string> | An optional list of libraries to be installed on the cluster. The default value is an empty list. |
| `settings.tasks[].for_each_task.task.max_retries` | number | An optional maximum number of times to retry an unsuccessful run. A run is considered to be unsuccessful if it completes with the `FAILED` result_state or `INTERNAL_ERROR` `life_cycle_state`. The value `-1` means to retry indefinitely and the value `0` means to never retry. |
| `settings.tasks[].for_each_task.task.min_retry_interval_millis` | number | An optional minimal interval in milliseconds between the start of the failed run and the subsequent retry run. The default behavior is that unsuccessful runs are immediately retried. |
| `settings.tasks[].for_each_task.task.new_cluster` | object | Contains a snapshot of the latest user specified settings that were used to create/edit the cluster. |
| `settings.tasks[].for_each_task.task.notebook_task` | object |  |
| `settings.tasks[].for_each_task.task.notification_settings` | object |  |
| `settings.tasks[].for_each_task.task.pipeline_task` | object |  |
| `settings.tasks[].for_each_task.task.power_bi_task` | object |  |
| `settings.tasks[].for_each_task.task.python_wheel_task` | object |  |
| `settings.tasks[].for_each_task.task.retry_on_timeout` | boolean | An optional policy to specify whether to retry a job when it times out. The default behavior is to not retry on timeout. |
| `settings.tasks[].for_each_task.task.run_if` | string | An optional value indicating the condition that determines whether the task should be run once its dependencies have been completed. When omitted, defaults to `ALL_SUCCESS`.  Possible values are: * `ALL_SUCCESS`: All dependencies have executed and succeeded * `AT_LEAST_ONE_SUCCESS`: At least one dependency has succeeded * `NONE_FAILED`: None of the dependencies have failed and at least one was executed * `ALL_DONE`: All dependencies have been completed * `AT_LEAST_ONE_FAILED`: At least one dependency failed * `ALL_FAILED`: ALl dependencies have failed |
| `settings.tasks[].for_each_task.task.run_job_task` | object |  |
| `settings.tasks[].for_each_task.task.spark_jar_task` | object |  |
| `settings.tasks[].for_each_task.task.spark_python_task` | object |  |
| `settings.tasks[].for_each_task.task.spark_submit_task` | object |  |
| `settings.tasks[].for_each_task.task.sql_task` | object |  |
| `settings.tasks[].for_each_task.task.task_key` | string | A unique name for the task. This field is used to refer to this task from other tasks. This field is required and must be unique within its parent job. On Update or Reset, this field is used to reference the tasks to be updated or reset. |
| `settings.tasks[].for_each_task.task.timeout_seconds` | number | An optional timeout applied to each run of this job task. A value of `0` means no timeout. |
| `settings.tasks[].for_each_task.task.webhook_notifications` | object |  |
| `settings.tasks[].health` | object | An optional set of health rules that can be defined for this job. |
| `settings.tasks[].health.rules` | array<string> |  |
| `settings.tasks[].health.rules[].metric` | string | Specifies the health metric that is being evaluated for a particular health rule.  * `RUN_DURATION_SECONDS`: Expected total time for a run in seconds. * `STREAMING_BACKLOG_BYTES`: An estimate of the maximum bytes of data waiting to be consumed across all streams. This metric is in Public Preview. * `STREAMING_BACKLOG_RECORDS`: An estimate of the maximum offset lag across all streams. This metric is in Public Preview. * `STREAMING_BACKLOG_SECONDS`: An estimate of the maximum consumer delay across all streams. This metric is in Public Preview. * `STREAMING_BACKLOG_FILES`: An estimate of the maximum number of outstanding files across all streams. This metric is in Public Preview. |
| `settings.tasks[].health.rules[].op` | string | Specifies the operator used to compare the health metric value with the specified threshold. |
| `settings.tasks[].health.rules[].value` | number | Specifies the threshold value that the health metric should obey to satisfy the health rule. |
| `settings.tasks[].job_cluster_key` | string | If job_cluster_key, this task is executed reusing the cluster specified in `job.settings.job_clusters`. |
| `settings.tasks[].libraries` | array<string> | An optional list of libraries to be installed on the cluster. The default value is an empty list. |
| `settings.tasks[].libraries[].cran` | object |  |
| `settings.tasks[].libraries[].cran.package` | string | The name of the CRAN package to install. |
| `settings.tasks[].libraries[].cran.repo` | string | The repository where the package can be found. If not specified, the default CRAN repo is used. |
| `settings.tasks[].libraries[].egg` | string | Deprecated. URI of the egg library to install. Installing Python egg files is deprecated and is not supported in Databricks Runtime 14.0 and above. |
| `settings.tasks[].libraries[].jar` | string | URI of the JAR library to install. Supported URIs include Workspace paths, Unity Catalog Volumes paths, and S3 URIs. For example: `{ "jar": "/Workspace/path/to/library.jar" }`, `{ "jar" : "/Volumes/path/to/library.jar" }` or `{ "jar": "s3://my-bucket/library.jar" }`. If S3 is used, please make sure the cluster has read access on the library. You may need to launch the cluster with an IAM role to access the S3 URI. |
| `settings.tasks[].libraries[].maven` | object |  |
| `settings.tasks[].libraries[].maven.coordinates` | string | Gradle-style maven coordinates. For example: "org.jsoup:jsoup:1.7.2". |
| `settings.tasks[].libraries[].maven.exclusions` | array<string> | List of dependences to exclude. For example: `["slf4j:slf4j", "*:hadoop-client"]`.  Maven dependency exclusions: https://maven.apache.org/guides/introduction/introduction-to-optional-and-excludes-dependencies.html. |
| `settings.tasks[].libraries[].maven.repo` | string | Maven repo to install the Maven package from. If omitted, both Maven Central Repository and Spark Packages are searched. |
| `settings.tasks[].libraries[].pypi` | object |  |
| `settings.tasks[].libraries[].pypi.package` | string | The name of the pypi package to install. An optional exact version specification is also supported. Examples: "simplejson" and "simplejson==3.8.0". |
| `settings.tasks[].libraries[].pypi.repo` | string | The repository where the package can be found. If not specified, the default pip index is used. |
| `settings.tasks[].libraries[].requirements` | string | URI of the requirements.txt file to install. Only Workspace paths and Unity Catalog Volumes paths are supported. For example: `{ "requirements": "/Workspace/path/to/requirements.txt" }` or `{ "requirements" : "/Volumes/path/to/requirements.txt" }` |
| `settings.tasks[].libraries[].whl` | string | URI of the wheel library to install. Supported URIs include Workspace paths, Unity Catalog Volumes paths, and S3 URIs. For example: `{ "whl": "/Workspace/path/to/library.whl" }`, `{ "whl" : "/Volumes/path/to/library.whl" }` or `{ "whl": "s3://my-bucket/library.whl" }`. If S3 is used, please make sure the cluster has read access on the library. You may need to launch the cluster with an IAM role to access the S3 URI. |
| `settings.tasks[].max_retries` | number | An optional maximum number of times to retry an unsuccessful run. A run is considered to be unsuccessful if it completes with the `FAILED` result_state or `INTERNAL_ERROR` `life_cycle_state`. The value `-1` means to retry indefinitely and the value `0` means to never retry. |
| `settings.tasks[].min_retry_interval_millis` | number | An optional minimal interval in milliseconds between the start of the failed run and the subsequent retry run. The default behavior is that unsuccessful runs are immediately retried. |
| `settings.tasks[].new_cluster` | object | Contains a snapshot of the latest user specified settings that were used to create/edit the cluster. |
| `settings.tasks[].new_cluster.apply_policy_default_values` | boolean | When set to true, fixed and default values from the policy will be used for fields that are omitted. When set to false, only fixed values from the policy will be applied. |
| `settings.tasks[].new_cluster.autoscale` | object |  |
| `settings.tasks[].new_cluster.autoscale.max_workers` | number | The maximum number of workers to which the cluster can scale up when overloaded. Note that `max_workers` must be strictly greater than `min_workers`. |
| `settings.tasks[].new_cluster.autoscale.min_workers` | number | The minimum number of workers to which the cluster can scale down when underutilized. It is also the initial number of workers the cluster will have after creation. |
| `settings.tasks[].new_cluster.autotermination_minutes` | number | Automatically terminates the cluster after it is inactive for this time in minutes. If not set, this cluster will not be automatically terminated. If specified, the threshold must be between 10 and 10000 minutes. Users can also set this value to 0 to explicitly disable automatic termination. |
| `settings.tasks[].new_cluster.aws_attributes` | object | Attributes set during cluster creation which are related to Amazon Web Services. |
| `settings.tasks[].new_cluster.aws_attributes.availability` | string | Availability type used for all subsequent nodes past the `first_on_demand` ones.  Note: If `first_on_demand` is zero, this availability type will be used for the entire cluster. |
| `settings.tasks[].new_cluster.aws_attributes.ebs_volume_count` | number | The number of volumes launched for each instance. Users can choose up to 10 volumes. This feature is only enabled for supported node types. Legacy node types cannot specify custom EBS volumes. For node types with no instance store, at least one EBS volume needs to be specified; otherwise, cluster creation will fail.  These EBS volumes will be mounted at `/ebs0`, `/ebs1`, and etc. Instance store volumes will be mounted at `/local_disk0`, `/local_disk1`, and etc.  If EBS volumes are attached, Databricks will configure Spark to use only the EBS volumes for scratch storage because heterogenously sized scratch devices can lead to inefficient disk utilization. If no EBS volumes are attached, Databricks will configure Spark to use instance store volumes.  Please note that if EBS volumes are specified, then the Spark configuration `spark.local.dir` will be overridden. |
| `settings.tasks[].new_cluster.aws_attributes.ebs_volume_iops` | number | If using gp3 volumes, what IOPS to use for the disk. If this is not set, the maximum performance of a gp2 volume with the same volume size will be used. |
| `settings.tasks[].new_cluster.aws_attributes.ebs_volume_size` | number | The size of each EBS volume (in GiB) launched for each instance. For general purpose SSD, this value must be within the range 100 - 4096. For throughput optimized HDD, this value must be within the range 500 - 4096. |
| `settings.tasks[].new_cluster.aws_attributes.ebs_volume_throughput` | number | If using gp3 volumes, what throughput to use for the disk. If this is not set, the maximum performance of a gp2 volume with the same volume size will be used. |
| `settings.tasks[].new_cluster.aws_attributes.ebs_volume_type` | string | All EBS volume types that Databricks supports. See https://aws.amazon.com/ebs/details/ for details. |
| `settings.tasks[].new_cluster.aws_attributes.first_on_demand` | number | The first `first_on_demand` nodes of the cluster will be placed on on-demand instances. If this value is greater than 0, the cluster driver node in particular will be placed on an on-demand instance. If this value is greater than or equal to the current cluster size, all nodes will be placed on on-demand instances. If this value is less than the current cluster size, `first_on_demand` nodes will be placed on on-demand instances and the remainder will be placed on `availability` instances. Note that this value does not affect cluster size and cannot currently be mutated over the lifetime of a cluster. |
| `settings.tasks[].new_cluster.aws_attributes.instance_profile_arn` | string | Nodes for this cluster will only be placed on AWS instances with this instance profile. If ommitted, nodes will be placed on instances without an IAM instance profile. The instance profile must have previously been added to the Databricks environment by an account administrator.  This feature may only be available to certain customer plans. |
| `settings.tasks[].new_cluster.aws_attributes.spot_bid_price_percent` | number | The bid price for AWS spot instances, as a percentage of the corresponding instance type's on-demand price. For example, if this field is set to 50, and the cluster needs a new `r3.xlarge` spot instance, then the bid price is half of the price of on-demand `r3.xlarge` instances. Similarly, if this field is set to 200, the bid price is twice the price of on-demand `r3.xlarge` instances. If not specified, the default value is 100. When spot instances are requested for this cluster, only spot instances whose bid price percentage matches this field will be considered. Note that, for safety, we enforce this field to be no more than 10000. |
| `settings.tasks[].new_cluster.aws_attributes.zone_id` | string | Identifier for the availability zone/datacenter in which the cluster resides. This string will be of a form like "us-west-2a". The provided availability zone must be in the same region as the Databricks deployment. For example, "us-west-2a" is not a valid zone id if the Databricks deployment resides in the "us-east-1" region. This is an optional field at cluster creation, and if not specified, the zone "auto" will be used. If the zone specified is "auto", will try to place cluster in a zone with high availability, and will retry placement in a different AZ if there is not enough capacity.  The list of available zones as well as the default value can be found by using the `List Zones` method. |
| `settings.tasks[].new_cluster.cluster_log_conf` | object | Cluster log delivery config |
| `settings.tasks[].new_cluster.cluster_log_conf.dbfs` | object | A storage location in DBFS |
| `settings.tasks[].new_cluster.cluster_log_conf.s3` | object | A storage location in Amazon S3 |
| `settings.tasks[].new_cluster.cluster_log_conf.volumes` | object | A storage location back by UC Volumes. |
| `settings.tasks[].new_cluster.cluster_name` | string | Cluster name requested by the user. This doesn't have to be unique. If not specified at creation, the cluster name will be an empty string. For job clusters, the cluster name is automatically set based on the job and job run IDs. |
| `settings.tasks[].new_cluster.custom_tags` | object | Additional tags for cluster resources. Databricks will tag all cluster resources (e.g., AWS instances and EBS volumes) with these tags in addition to `default_tags`. Notes:  - Currently, Databricks allows at most 45 custom tags  - Clusters can only reuse cloud resources if the resources' tags are a subset of the cluster tags |
| `settings.tasks[].new_cluster.data_security_mode` | string | Data security mode decides what data governance model to use when accessing data from a cluster.  The following modes can only be used when `kind = CLASSIC_PREVIEW`. * `DATA_SECURITY_MODE_AUTO`: Databricks will choose the most appropriate access mode depending on your compute configuration. * `DATA_SECURITY_MODE_STANDARD`: Alias for `USER_ISOLATION`. * `DATA_SECURITY_MODE_DEDICATED`: Alias for `SINGLE_USER`.  The following modes can be used regardless of `kind`. * `NONE`: No security isolation for multiple users sharing the cluster. Data governance features are not available in this mode. * `SINGLE_USER`: A secure cluster that can only be exclusively used by a single user specified in `single_user_name`. Most programming languages, cluster features and data governance features are available in this mode. * `USER_ISOLATION`: A secure cluster that can be shared by multiple users. Cluster users are fully isolated so that they cannot see each other's data and credentials. Most data governance features are supported in this mode. But programming languages and cluster features might be limited.  The following modes are deprecated starting with Databricks Runtime 15.0 and will be removed for future Databricks Runtime versions:  * `LEGACY_TABLE_ACL`: This mode is for users migrating from legacy Table ACL clusters. * `LEGACY_PASSTHROUGH`: This mode is for users migrating from legacy Passthrough on high concurrency clusters. * `LEGACY_SINGLE_USER`: This mode is for users migrating from legacy Passthrough on standard clusters. * `LEGACY_SINGLE_USER_STANDARD`: This mode provides a way that doesnât have UC nor passthrough enabled. |
| `settings.tasks[].new_cluster.docker_image` | object |  |
| `settings.tasks[].new_cluster.docker_image.basic_auth` | object |  |
| `settings.tasks[].new_cluster.docker_image.url` | string | URL of the docker image. |
| `settings.tasks[].new_cluster.driver_instance_pool_id` | string | The optional ID of the instance pool for the driver of the cluster belongs. The pool cluster uses the instance pool with id (instance_pool_id) if the driver pool is not assigned. |
| `settings.tasks[].new_cluster.driver_node_type_flexibility` | object | Configuration for flexible node types, allowing fallback to alternate node types during cluster launch and upscale. |
| `settings.tasks[].new_cluster.driver_node_type_flexibility.alternate_node_type_ids` | array<string> | A list of node type IDs to use as fallbacks when the primary node type is unavailable. |
| `settings.tasks[].new_cluster.driver_node_type_id` | string | The node type of the Spark driver. Note that this field is optional; if unset, the driver node type will be set as the same value as `node_type_id` defined above.  This field, along with node_type_id, should not be set if virtual_cluster_size is set. If both driver_node_type_id, node_type_id, and virtual_cluster_size are specified, driver_node_type_id and node_type_id take precedence. |
| `settings.tasks[].new_cluster.enable_elastic_disk` | boolean | Autoscaling Local Storage: when enabled, this cluster will dynamically acquire additional disk space when its Spark workers are running low on disk space.  This feature requires specific AWS permissions to function correctly - refer to the User Guide for more details. |
| `settings.tasks[].new_cluster.enable_local_disk_encryption` | boolean | Whether to enable LUKS on cluster VMs' local disks |
| `settings.tasks[].new_cluster.init_scripts` | array<string> | The configuration for storing init scripts. Any number of destinations can be specified. The scripts are executed sequentially in the order provided. If `cluster_log_conf` is specified, init script logs are sent to `<destination>/<cluster-ID>/init_scripts`. |
| `settings.tasks[].new_cluster.init_scripts[].abfss` | object | A storage location in Adls Gen2 |
| `settings.tasks[].new_cluster.init_scripts[].dbfs` | object | A storage location in DBFS |
| `settings.tasks[].new_cluster.init_scripts[].file` | object |  |
| `settings.tasks[].new_cluster.init_scripts[].gcs` | object | A storage location in Google Cloud Platform's GCS |
| `settings.tasks[].new_cluster.init_scripts[].s3` | object | A storage location in Amazon S3 |
| `settings.tasks[].new_cluster.init_scripts[].volumes` | object | A storage location back by UC Volumes. |
| `settings.tasks[].new_cluster.init_scripts[].workspace` | object | A storage location in Workspace Filesystem (WSFS) |
| `settings.tasks[].new_cluster.instance_pool_id` | string | The optional ID of the instance pool to which the cluster belongs. |
| `settings.tasks[].new_cluster.is_single_node` | boolean | This field can only be used when `kind = CLASSIC_PREVIEW`.  When set to true, Databricks will automatically set single node related `custom_tags`, `spark_conf`, and `num_workers` |
| `settings.tasks[].new_cluster.kind` | string | The kind of compute described by this compute specification.  Depending on `kind`, different validations and default values will be applied.  Clusters with `kind = CLASSIC_PREVIEW` support the following fields, whereas clusters with no specified `kind` do not. * [is_single_node](/api/workspace/clusters/create#is_single_node) * [use_ml_runtime](/api/workspace/clusters/create#use_ml_runtime) * [data_security_mode](/api/workspace/clusters/create#data_security_mode) set to `DATA_SECURITY_MODE_AUTO`, `DATA_SECURITY_MODE_DEDICATED`, or `DATA_SECURITY_MODE_STANDARD`  By using the [simple form](https://docs.databricks.com/compute/simple-form.html), your clusters are automatically using `kind = CLASSIC_PREVIEW`. |
| `settings.tasks[].new_cluster.node_type_id` | string | This field encodes, through a single value, the resources available to each of the Spark nodes in this cluster. For example, the Spark nodes can be provisioned and optimized for memory or compute intensive workloads. A list of available node types can be retrieved by using the :method:clusters/listNodeTypes API call. |
| `settings.tasks[].new_cluster.num_workers` | number | Number of worker nodes that this cluster should have. A cluster has one Spark Driver and `num_workers` Executors for a total of `num_workers` + 1 Spark nodes.  Note: When reading the properties of a cluster, this field reflects the desired number of workers rather than the actual current number of workers. For instance, if a cluster is resized from 5 to 10 workers, this field will immediately be updated to reflect the target size of 10 workers, whereas the workers listed in `spark_info` will gradually increase from 5 to 10 as the new nodes are provisioned. |
| `settings.tasks[].new_cluster.policy_id` | string | The ID of the cluster policy used to create the cluster if applicable. |
| `settings.tasks[].new_cluster.runtime_engine` | string |  |
| `settings.tasks[].new_cluster.single_user_name` | string | Single user name if data_security_mode is `SINGLE_USER` |
| `settings.tasks[].new_cluster.spark_conf` | object | An object containing a set of optional, user-specified Spark configuration key-value pairs. Users can also pass in a string of extra JVM options to the driver and the executors via `spark.driver.extraJavaOptions` and `spark.executor.extraJavaOptions` respectively. |
| `settings.tasks[].new_cluster.spark_env_vars` | object | An object containing a set of optional, user-specified environment variable key-value pairs. Please note that key-value pair of the form (X,Y) will be exported as is (i.e., `export X='Y'`) while launching the driver and workers.  In order to specify an additional set of `SPARK_DAEMON_JAVA_OPTS`, we recommend appending them to `$SPARK_DAEMON_JAVA_OPTS` as shown in the example below. This ensures that all default databricks managed environmental variables are included as well.  Example Spark environment variables: `{"SPARK_WORKER_MEMORY": "28000m", "SPARK_LOCAL_DIRS": "/local_disk0"}` or `{"SPARK_DAEMON_JAVA_OPTS": "$SPARK_DAEMON_JAVA_OPTS -Dspark.shuffle.service.enabled=true"}` |
| `settings.tasks[].new_cluster.spark_version` | string | The Spark version of the cluster, e.g. `3.3.x-scala2.11`. A list of available Spark versions can be retrieved by using the :method:clusters/sparkVersions API call. |
| `settings.tasks[].new_cluster.ssh_public_keys` | array<string> | SSH public key contents that will be added to each Spark node in this cluster. The corresponding private keys can be used to login with the user name `ubuntu` on port `2200`. Up to 10 keys can be specified. |
| `settings.tasks[].new_cluster.use_ml_runtime` | boolean | This field can only be used when `kind = CLASSIC_PREVIEW`.  `effective_spark_version` is determined by `spark_version` (DBR release), this field `use_ml_runtime`, and whether `node_type_id` is gpu node or not. |
| `settings.tasks[].new_cluster.worker_node_type_flexibility` | object | Configuration for flexible node types, allowing fallback to alternate node types during cluster launch and upscale. |
| `settings.tasks[].new_cluster.worker_node_type_flexibility.alternate_node_type_ids` | array<string> | A list of node type IDs to use as fallbacks when the primary node type is unavailable. |
| `settings.tasks[].new_cluster.workload_type` | object | Cluster Attributes showing for clusters workload types. |
| `settings.tasks[].new_cluster.workload_type.clients` | object |  |
| `settings.tasks[].notebook_task` | object |  |
| `settings.tasks[].notebook_task.base_parameters` | object | Base parameters to be used for each run of this job. If the run is initiated by a call to :method:jobs/run Now with parameters specified, the two parameters maps are merged. If the same key is specified in `base_parameters` and in `run-now`, the value from `run-now` is used. Use [Task parameter variables](https://docs.databricks.com/jobs.html#parameter-variables) to set parameters containing information about job runs.  If the notebook takes a parameter that is not specified in the jobâs `base_parameters` or the `run-now` override parameters, the default value from the notebook is used.  Retrieve these parameters in a notebook using [dbutils.widgets.get](https://docs.databricks.com/dev-tools/databricks-utils.html#dbutils-widgets).  The JSON representation of this field cannot exceed 1MB. |
| `settings.tasks[].notebook_task.notebook_path` | string | The path of the notebook to be run in the Databricks workspace or remote repository. For notebooks stored in the Databricks workspace, the path must be absolute and begin with a slash. For notebooks stored in a remote repository, the path must be relative. This field is required. |
| `settings.tasks[].notebook_task.source` | string | Optional location type of the SQL file. When set to `WORKSPACE`, the SQL file will be retrieved\ from the local Databricks workspace. When set to `GIT`, the SQL file will be retrieved from a Git repository defined in `git_source`. If the value is empty, the task will use `GIT` if `git_source` is defined and `WORKSPACE` otherwise.  * `WORKSPACE`: SQL file is located in Databricks workspace. * `GIT`: SQL file is located in cloud Git provider. |
| `settings.tasks[].notebook_task.warehouse_id` | string | Optional `warehouse_id` to run the notebook on a SQL warehouse. Classic SQL warehouses are NOT supported, please use serverless or pro SQL warehouses.  Note that SQL warehouses only support SQL cells; if the notebook contains non-SQL cells, the run will fail. |
| `settings.tasks[].notification_settings` | object |  |
| `settings.tasks[].notification_settings.alert_on_last_attempt` | boolean | If true, do not send notifications to recipients specified in `on_start` for the retried runs and do not send notifications to recipients specified in `on_failure` until the last retry of the run. |
| `settings.tasks[].notification_settings.no_alert_for_canceled_runs` | boolean | If true, do not send notifications to recipients specified in `on_failure` if the run is canceled. |
| `settings.tasks[].notification_settings.no_alert_for_skipped_runs` | boolean | If true, do not send notifications to recipients specified in `on_failure` if the run is skipped. |
| `settings.tasks[].pipeline_task` | object |  |
| `settings.tasks[].pipeline_task.full_refresh` | boolean | If true, triggers a full refresh on the delta live table. |
| `settings.tasks[].pipeline_task.pipeline_id` | string | The full name of the pipeline task to execute. |
| `settings.tasks[].power_bi_task` | object |  |
| `settings.tasks[].power_bi_task.connection_resource_name` | string | The resource name of the UC connection to authenticate from Databricks to Power BI |
| `settings.tasks[].power_bi_task.power_bi_model` | object |  |
| `settings.tasks[].power_bi_task.power_bi_model.authentication_method` | string |  |
| `settings.tasks[].power_bi_task.power_bi_model.model_name` | string | The name of the Power BI model |
| `settings.tasks[].power_bi_task.power_bi_model.overwrite_existing` | boolean | Whether to overwrite existing Power BI models |
| `settings.tasks[].power_bi_task.power_bi_model.storage_mode` | string |  |
| `settings.tasks[].power_bi_task.power_bi_model.workspace_name` | string | The name of the Power BI workspace of the model |
| `settings.tasks[].power_bi_task.refresh_after_update` | boolean | Whether the model should be refreshed after the update |
| `settings.tasks[].power_bi_task.tables` | array<string> | The tables to be exported to Power BI |
| `settings.tasks[].power_bi_task.tables[].catalog` | string | The catalog name in Databricks |
| `settings.tasks[].power_bi_task.tables[].name` | string | The table name in Databricks |
| `settings.tasks[].power_bi_task.tables[].schema` | string | The schema name in Databricks |
| `settings.tasks[].power_bi_task.tables[].storage_mode` | string |  |
| `settings.tasks[].power_bi_task.warehouse_id` | string | The SQL warehouse ID to use as the Power BI data source |
| `settings.tasks[].python_wheel_task` | object |  |
| `settings.tasks[].python_wheel_task.entry_point` | string | Named entry point to use, if it does not exist in the metadata of the package it executes the function from the package directly using `$packageName.$entryPoint()` |
| `settings.tasks[].python_wheel_task.named_parameters` | object | Command-line parameters passed to Python wheel task in the form of `["--name=task", "--data=dbfs:/path/to/data.json"]`. Leave it empty if `parameters` is not null. |
| `settings.tasks[].python_wheel_task.package_name` | string | Name of the package to execute |
| `settings.tasks[].python_wheel_task.parameters` | array<string> | Command-line parameters passed to Python wheel task. Leave it empty if `named_parameters` is not null. |
| `settings.tasks[].retry_on_timeout` | boolean | An optional policy to specify whether to retry a job when it times out. The default behavior is to not retry on timeout. |
| `settings.tasks[].run_if` | string | An optional value indicating the condition that determines whether the task should be run once its dependencies have been completed. When omitted, defaults to `ALL_SUCCESS`.  Possible values are: * `ALL_SUCCESS`: All dependencies have executed and succeeded * `AT_LEAST_ONE_SUCCESS`: At least one dependency has succeeded * `NONE_FAILED`: None of the dependencies have failed and at least one was executed * `ALL_DONE`: All dependencies have been completed * `AT_LEAST_ONE_FAILED`: At least one dependency failed * `ALL_FAILED`: ALl dependencies have failed |
| `settings.tasks[].run_job_task` | object |  |
| `settings.tasks[].run_job_task.job_id` | number | ID of the job to trigger. |
| `settings.tasks[].run_job_task.job_parameters` | object | Job-level parameters used to trigger the job. |
| `settings.tasks[].run_job_task.pipeline_params` | object |  |
| `settings.tasks[].run_job_task.pipeline_params.full_refresh` | boolean | If true, triggers a full refresh on the delta live table. |
| `settings.tasks[].spark_jar_task` | object |  |
| `settings.tasks[].spark_jar_task.jar_uri` | string | Deprecated since 04/2016. For classic compute, provide a `jar` through the `libraries` field instead. For serverless compute, provide a `jar` though the `java_dependencies` field inside the `environments` list.  See the examples of classic and serverless compute usage at the top of the page. |
| `settings.tasks[].spark_jar_task.main_class_name` | string | The full name of the class containing the main method to be executed. This class must be contained in a JAR provided as a library.  The code must use `SparkContext.getOrCreate` to obtain a Spark context; otherwise, runs of the job fail. |
| `settings.tasks[].spark_jar_task.parameters` | array<string> | Parameters passed to the main method.  Use [Task parameter variables](https://docs.databricks.com/jobs.html#parameter-variables) to set parameters containing information about job runs. |
| `settings.tasks[].spark_jar_task.run_as_repl` | boolean | Deprecated. A value of `false` is no longer supported. |
| `settings.tasks[].spark_python_task` | object |  |
| `settings.tasks[].spark_python_task.parameters` | array<string> | Command line parameters passed to the Python file.  Use [Task parameter variables](https://docs.databricks.com/jobs.html#parameter-variables) to set parameters containing information about job runs. |
| `settings.tasks[].spark_python_task.python_file` | string | The Python file to be executed. Cloud file URIs (such as dbfs:/, s3:/, adls:/, gcs:/) and workspace paths are supported. For python files stored in the Databricks workspace, the path must be absolute and begin with `/`. For files stored in a remote repository, the path must be relative. This field is required. |
| `settings.tasks[].spark_python_task.source` | string | Optional location type of the SQL file. When set to `WORKSPACE`, the SQL file will be retrieved\ from the local Databricks workspace. When set to `GIT`, the SQL file will be retrieved from a Git repository defined in `git_source`. If the value is empty, the task will use `GIT` if `git_source` is defined and `WORKSPACE` otherwise.  * `WORKSPACE`: SQL file is located in Databricks workspace. * `GIT`: SQL file is located in cloud Git provider. |
| `settings.tasks[].spark_submit_task` | object |  |
| `settings.tasks[].spark_submit_task.parameters` | array<string> | Command-line parameters passed to spark submit.  Use [Task parameter variables](https://docs.databricks.com/jobs.html#parameter-variables) to set parameters containing information about job runs. |
| `settings.tasks[].sql_task` | object |  |
| `settings.tasks[].sql_task.alert` | object |  |
| `settings.tasks[].sql_task.alert.alert_id` | string | The canonical identifier of the SQL alert. |
| `settings.tasks[].sql_task.alert.pause_subscriptions` | boolean | If true, the alert notifications are not sent to subscribers. |
| `settings.tasks[].sql_task.alert.subscriptions` | array<string> | If specified, alert notifications are sent to subscribers. |
| `settings.tasks[].sql_task.dashboard` | object |  |
| `settings.tasks[].sql_task.dashboard.custom_subject` | string | Subject of the email sent to subscribers of this task. |
| `settings.tasks[].sql_task.dashboard.dashboard_id` | string | The canonical identifier of the SQL dashboard. |
| `settings.tasks[].sql_task.dashboard.pause_subscriptions` | boolean | If true, the dashboard snapshot is not taken, and emails are not sent to subscribers. |
| `settings.tasks[].sql_task.dashboard.subscriptions` | array<string> | If specified, dashboard snapshots are sent to subscriptions. |
| `settings.tasks[].sql_task.file` | object |  |
| `settings.tasks[].sql_task.file.path` | string | Path of the SQL file. Must be relative if the source is a remote Git repository and absolute for workspace paths. |
| `settings.tasks[].sql_task.file.source` | string | Optional location type of the SQL file. When set to `WORKSPACE`, the SQL file will be retrieved\ from the local Databricks workspace. When set to `GIT`, the SQL file will be retrieved from a Git repository defined in `git_source`. If the value is empty, the task will use `GIT` if `git_source` is defined and `WORKSPACE` otherwise.  * `WORKSPACE`: SQL file is located in Databricks workspace. * `GIT`: SQL file is located in cloud Git provider. |
| `settings.tasks[].sql_task.parameters` | object | Parameters to be used for each run of this job. The SQL alert task does not support custom parameters. |
| `settings.tasks[].sql_task.query` | object |  |
| `settings.tasks[].sql_task.query.query_id` | string | The canonical identifier of the SQL query. |
| `settings.tasks[].sql_task.warehouse_id` | string | The canonical identifier of the SQL warehouse. Recommended to use with serverless or pro SQL warehouses. Classic SQL warehouses are only supported for SQL alert, dashboard and query tasks and are limited to scheduled single-task jobs. |
| `settings.tasks[].task_key` | string | A unique name for the task. This field is used to refer to this task from other tasks. This field is required and must be unique within its parent job. On Update or Reset, this field is used to reference the tasks to be updated or reset. |
| `settings.tasks[].timeout_seconds` | number | An optional timeout applied to each run of this job task. A value of `0` means no timeout. |
| `settings.tasks[].webhook_notifications` | object |  |
| `settings.tasks[].webhook_notifications.on_duration_warning_threshold_exceeded` | array<string> | An optional list of system notification IDs to call when the duration of a run exceeds the threshold specified for the `RUN_DURATION_SECONDS` metric in the `health` field. A maximum of 3 destinations can be specified for the `on_duration_warning_threshold_exceeded` property. |
| `settings.tasks[].webhook_notifications.on_duration_warning_threshold_exceeded[].id` | string |  |
| `settings.tasks[].webhook_notifications.on_failure` | array<string> | An optional list of system notification IDs to call when the run fails. A maximum of 3 destinations can be specified for the `on_failure` property. |
| `settings.tasks[].webhook_notifications.on_failure[].id` | string |  |
| `settings.tasks[].webhook_notifications.on_start` | array<string> | An optional list of system notification IDs to call when the run starts. A maximum of 3 destinations can be specified for the `on_start` property. |
| `settings.tasks[].webhook_notifications.on_start[].id` | string |  |
| `settings.tasks[].webhook_notifications.on_streaming_backlog_exceeded` | array<string> | An optional list of system notification IDs to call when any streaming backlog thresholds are exceeded for any stream. Streaming backlog thresholds can be set in the `health` field using the following metrics: `STREAMING_BACKLOG_BYTES`, `STREAMING_BACKLOG_RECORDS`, `STREAMING_BACKLOG_SECONDS`, or `STREAMING_BACKLOG_FILES`. Alerting is based on the 10-minute average of these metrics. If the issue persists, notifications are resent every 30 minutes. A maximum of 3 destinations can be specified for the `on_streaming_backlog_exceeded` property. |
| `settings.tasks[].webhook_notifications.on_streaming_backlog_exceeded[].id` | string |  |
| `settings.tasks[].webhook_notifications.on_success` | array<string> | An optional list of system notification IDs to call when the run completes successfully. A maximum of 3 destinations can be specified for the `on_success` property. |
| `settings.tasks[].webhook_notifications.on_success[].id` | string |  |
| `settings.timeout_seconds` | number | An optional timeout applied to each run of this job. A value of `0` means no timeout. |
| `settings.trigger` | object |  |
| `settings.trigger.file_arrival` | object |  |
| `settings.trigger.file_arrival.min_time_between_triggers_seconds` | number | If set, the trigger starts a run only after the specified amount of time passed since the last time the trigger fired. The minimum allowed value is 60 seconds |
| `settings.trigger.file_arrival.url` | string | URL to be monitored for file arrivals. The path must point to the root or a subpath of the external location. |
| `settings.trigger.file_arrival.wait_after_last_change_seconds` | number | If set, the trigger starts a run only after no file activity has occurred for the specified amount of time. This makes it possible to wait for a batch of incoming files to arrive before triggering a run. The minimum allowed value is 60 seconds. |
| `settings.trigger.pause_status` | string |  |
| `settings.trigger.periodic` | object |  |
| `settings.trigger.periodic.interval` | number | The interval at which the trigger should run. |
| `settings.trigger.periodic.unit` | string |  |
| `settings.trigger.table_update` | object |  |
| `settings.trigger.table_update.condition` | string |  |
| `settings.trigger.table_update.min_time_between_triggers_seconds` | number | If set, the trigger starts a run only after the specified amount of time has passed since the last time the trigger fired. The minimum allowed value is 60 seconds. |
| `settings.trigger.table_update.table_names` | array<string> | A list of tables to monitor for changes. The table name must be in the format `catalog_name.schema_name.table_name`. |
| `settings.trigger.table_update.wait_after_last_change_seconds` | number | If set, the trigger starts a run only after no table updates have occurred for the specified time and can be used to wait for a series of table updates before triggering a run. The minimum allowed value is 60 seconds. |
| `settings.webhook_notifications` | object |  |
| `settings.webhook_notifications.on_duration_warning_threshold_exceeded` | array<string> | An optional list of system notification IDs to call when the duration of a run exceeds the threshold specified for the `RUN_DURATION_SECONDS` metric in the `health` field. A maximum of 3 destinations can be specified for the `on_duration_warning_threshold_exceeded` property. |
| `settings.webhook_notifications.on_duration_warning_threshold_exceeded[].id` | string |  |
| `settings.webhook_notifications.on_failure` | array<string> | An optional list of system notification IDs to call when the run fails. A maximum of 3 destinations can be specified for the `on_failure` property. |
| `settings.webhook_notifications.on_failure[].id` | string |  |
| `settings.webhook_notifications.on_start` | array<string> | An optional list of system notification IDs to call when the run starts. A maximum of 3 destinations can be specified for the `on_start` property. |
| `settings.webhook_notifications.on_start[].id` | string |  |
| `settings.webhook_notifications.on_streaming_backlog_exceeded` | array<string> | An optional list of system notification IDs to call when any streaming backlog thresholds are exceeded for any stream. Streaming backlog thresholds can be set in the `health` field using the following metrics: `STREAMING_BACKLOG_BYTES`, `STREAMING_BACKLOG_RECORDS`, `STREAMING_BACKLOG_SECONDS`, or `STREAMING_BACKLOG_FILES`. Alerting is based on the 10-minute average of these metrics. If the issue persists, notifications are resent every 30 minutes. A maximum of 3 destinations can be specified for the `on_streaming_backlog_exceeded` property. |
| `settings.webhook_notifications.on_streaming_backlog_exceeded[].id` | string |  |
| `settings.webhook_notifications.on_success` | array<string> | An optional list of system notification IDs to call when the run completes successfully. A maximum of 3 destinations can be specified for the `on_success` property. |
| `settings.webhook_notifications.on_success[].id` | string |  |
| `trigger_state` | object |  |
| `trigger_state.file_arrival` | object |  |
| `trigger_state.file_arrival.using_file_events` | boolean | Indicates whether the trigger leverages file events to detect file arrivals. |
| `trigger_state.table` | object |  |
| `trigger_state.table.last_seen_table_states` | array<string> |  |
| `trigger_state.table.last_seen_table_states[].has_seen_updates` | boolean | Whether or not the table has seen updates since either the creation of the trigger or the last successful evaluation of the trigger |
| `trigger_state.table.last_seen_table_states[].table_name` | string | Full table name of the table to monitor, e.g. `mycatalog.myschema.mytable` |
| `trigger_state.table.using_scalable_monitoring` | boolean | Indicates whether the trigger is using scalable monitoring. |

## Native endpoint

Through the native Databricks API, this operation is `GET {{credentials.host}}/api/2.2/jobs/list` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

