# Databricks: Create Pipeline

Creates a new pipeline in the Databricks workspace.

```
POST https://connect.mindcloud.co/v1/universal/databricks/latest/actions/create-pipeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/create-pipeline" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clusters": "string",
  "deployment.kind": "string",
  "libraries": "string",
  "notifications": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/databricks/latest/actions/create-pipeline', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clusters": "string",
    "deployment.kind": "string",
    "libraries": "string",
    "notifications": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowDuplicateNames` | boolean | no | If false, deployment will fail if name conflicts with that of another pipeline. |
| `budgetPolicyId` | string | no | Budget policy of this pipeline. |
| `catalog` | string | no | A catalog in Unity Catalog to publish data from this pipeline to. If `target` is specified, tables in this pipeline are published to a `target` schema inside `catalog` (for example, `catalog`.`target`.`table`). If `target` is not specified, no data is published to Unity Catalog. |
| `channel` | string | no | DLT Release Channel that specifies which version to use. |
| `clusters` | list<string> | yes | Cluster settings for this pipeline deployment. |
| `configuration` | object | no | String-String configuration for this pipeline execution. |
| `continuous` | boolean | no | Whether the pipeline is continuous or triggered. This replaces `trigger`. |
| `deployment` | object | no |  |
| `deployment.kind` | string | yes | The deployment method that manages the pipeline: - BUNDLE: The pipeline is managed by a Databricks Asset Bundle. |
| `deployment.metadataFilePath` | string | no | The path to the file containing metadata about the deployment. |
| `development` | boolean | no | Whether the pipeline is in Development mode. Defaults to false. |
| `dryRun` | boolean | no |  |
| `edition` | string | no | Pipeline product edition. |
| `environment` | object | no | The environment entity used to preserve serverless environment side panel, jobs' environment for non-notebook task, and DLT's environment for classic and serverless pipelines. In this minimal environment spec, only pip dependencies are supported. |
| `environment.dependencies` | list<string> | no | List of pip dependencies, as supported by the version of pip in this environment. Each dependency is a pip requirement file line https://pip.pypa.io/en/stable/reference/requirements-file-format/ Allowed dependency could be <requirement specifier>, <archive url/path>, <local project path>(WSFS or Volumes in Databricks), <vcs project url> |
| `eventLog` | object | no | Configurable event log parameters. |
| `eventLog.catalog` | string | no | The UC catalog the event log is published under. |
| `eventLog.name` | string | no | The name the event log is published to in UC. |
| `eventLog.schema` | string | no | The UC schema the event log is published under. |
| `filters` | object | no |  |
| `filters.exclude` | list<string> | no | Paths to exclude. |
| `filters.include` | list<string> | no | Paths to include. |
| `id` | string | no | Unique identifier for this pipeline. |
| `ingestionDefinition` | object | no |  |
| `ingestionDefinition.connectionName` | string | no | The Unity Catalog connection that this ingestion pipeline uses to communicate with the source. This is used with both connectors for applications like Salesforce, Workday, and so on, and also database connectors like Oracle, (connector_type = QUERY_BASED OR connector_type = CDC). If connection name corresponds to database connectors like Oracle, and connector_type is not provided then connector_type defaults to QUERY_BASED. If connector_type is passed as CDC we use Combined Cdc Managed Ingestion pipeline. Under certain conditions, this can be replaced with ingestion_gateway_id to change the connector to Cdc Managed Ingestion Pipeline with Gateway pipeline. |
| `ingestionDefinition.fullRefreshWindow` | object | no | Proto representing a window |
| `ingestionDefinition.ingestionGatewayId` | string | no | Identifier for the gateway that is used by this ingestion pipeline to communicate with the source database. This is used with CDC connectors to databases like SQL Server using a gateway pipeline (connector_type = CDC). Under certain conditions, this can be replaced with connection_name to change the connector to Combined Cdc Managed Ingestion Pipeline. |
| `ingestionDefinition.objects` | list<string> | no | Required. Settings specifying tables to replicate and the destination for the replicated tables. |
| `ingestionDefinition.sourceConfigurations` | list<string> | no | Top-level source configurations |
| `ingestionDefinition.sourceType` | string | no |  |
| `ingestionDefinition.tableConfiguration` | object | no |  |
| `libraries` | list<string> | yes | Libraries or code needed by this deployment. |
| `name` | string | no | Friendly identifier for this pipeline. |
| `notifications` | list<string> | yes | List of notification settings for this pipeline. |
| `photon` | boolean | no | Whether Photon is enabled for this pipeline. |
| `rootPath` | string | no | Root path for this pipeline. This is used as the root directory when editing the pipeline in the Databricks user interface and it is added to sys.path when executing Python sources during pipeline execution. |
| `runAs` | object | no | Write-only setting, available only in Create/Update calls. Specifies the user or service principal that the pipeline runs as. If not specified, the pipeline runs as the user who created the pipeline. Only `user_name` or `service_principal_name` can be specified. If both are specified, an error is thrown. |
| `runAs.servicePrincipalName` | string | no | Application ID of an active service principal. Setting this field requires the `servicePrincipal/user` role. |
| `runAs.userName` | string | no | The email of an active workspace user. Users can only set this field to their own email. |
| `schema` | string | no | The default schema (database) where tables are read from or published to. |
| `serverless` | boolean | no | Whether serverless compute is enabled for this pipeline. |
| `storage` | string | no | DBFS root directory for storing checkpoints and tables. |
| `tags` | object | no | A map of tags associated with the pipeline. These are forwarded to the cluster as cluster tags, and are therefore subject to the same limitations. A maximum of 25 tags can be added to the pipeline. |
| `target` | string | no | Target schema (database) to add tables in this pipeline to. Exactly one of `schema` or `target` must be specified. To publish to Unity Catalog, also specify `catalog`. This legacy field is deprecated for pipeline creation in favor of the `schema` field. |
| `trigger` | object | no |  |
| `trigger.cron` | object | no |  |
| `trigger.manual` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "effective_settings": {
        "budget_policy_id": "string",
        "catalog": "string",
        "channel": "string",
        "clusters": [
          {
            "apply_policy_default_values": true,
            "autoscale": {
              "max_workers": 1,
              "min_workers": 1,
              "mode": "string"
            },
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
              "dbfs": {
                "destination": "string"
              },
              "s3": {
                "canned_acl": "string",
                "destination": "string",
                "enable_encryption": true,
                "encryption_type": "string",
                "endpoint": "string",
                "kms_key": "string",
                "region": "string"
              },
              "volumes": {
                "destination": "string"
              }
            },
            "custom_tags": {},
            "driver_instance_pool_id": "string",
            "driver_node_type_id": "string",
            "enable_local_disk_encryption": true,
            "init_scripts": [
              {
                "abfss": {
                  "destination": "string"
                },
                "dbfs": {
                  "destination": "string"
                },
                "file": {
                  "destination": "string"
                },
                "gcs": {
                  "destination": "string"
                },
                "s3": {
                  "canned_acl": "string",
                  "destination": "string",
                  "enable_encryption": true,
                  "encryption_type": "string",
                  "endpoint": "string",
                  "kms_key": "string",
                  "region": "string"
                },
                "volumes": {
                  "destination": "string"
                },
                "workspace": {
                  "destination": "string"
                }
              }
            ],
            "instance_pool_id": "string",
            "label": "string",
            "node_type_id": "string",
            "num_workers": 1,
            "policy_id": "string",
            "spark_conf": {},
            "spark_env_vars": {},
            "ssh_public_keys": [
              "string"
            ]
          }
        ],
        "configuration": {},
        "continuous": true,
        "deployment": {
          "kind": "string",
          "metadata_file_path": "string"
        },
        "development": true,
        "edition": "string",
        "environment": {
          "dependencies": [
            "string"
          ]
        },
        "event_log": {
          "catalog": "string",
          "name": "Ava Chen",
          "schema": "string"
        },
        "filters": {
          "exclude": [
            "string"
          ],
          "include": [
            "string"
          ]
        },
        "id": "string",
        "ingestion_definition": {
          "connection_name": "Ava Chen",
          "full_refresh_window": {
            "days_of_week": [
              "string"
            ],
            "start_hour": 1,
            "time_zone_id": "string"
          },
          "ingestion_gateway_id": "string",
          "objects": [
            {
              "report": {
                "destination_catalog": "string",
                "destination_schema": "string",
                "destination_table": "string",
                "source_url": "https://example.com",
                "table_configuration": {}
              },
              "schema": {
                "destination_catalog": "string",
                "destination_schema": "string",
                "source_catalog": "string",
                "source_schema": "string",
                "table_configuration": {}
              },
              "table": {
                "destination_catalog": "string",
                "destination_schema": "string",
                "destination_table": "string",
                "source_catalog": "string",
                "source_schema": "string",
                "source_table": "string",
                "table_configuration": {}
              }
            }
          ],
          "source_configurations": [
            {
              "catalog": {
                "postgres": {},
                "source_catalog": "string"
              }
            }
          ],
          "source_type": "string",
          "table_configuration": {
            "auto_full_refresh_policy": {
              "enabled": true,
              "min_interval_hours": 1
            },
            "exclude_columns": [
              "string"
            ],
            "include_columns": [
              "string"
            ],
            "primary_keys": [
              "string"
            ],
            "sequence_by": [
              "string"
            ]
          }
        },
        "libraries": [
          {
            "file": {
              "path": "string"
            },
            "glob": {
              "include": "string"
            },
            "notebook": {
              "path": "string"
            },
            "whl": "string"
          }
        ],
        "name": "Ava Chen",
        "notifications": [
          {
            "alerts": [
              "string"
            ],
            "email_recipients": [
              "ava@example.com"
            ]
          }
        ],
        "photon": true,
        "root_path": "string",
        "schema": "string",
        "serverless": true,
        "storage": "string",
        "tags": {},
        "target": "string",
        "trigger": {
          "cron": {
            "quartz_cron_schedule": "string",
            "timezone_id": "string"
          },
          "manual": {}
        }
      },
      "pipeline_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `effective_settings` | object |  |
| `effective_settings.budget_policy_id` | string | Budget policy of this pipeline. |
| `effective_settings.catalog` | string | A catalog in Unity Catalog to publish data from this pipeline to. If `target` is specified, tables in this pipeline are published to a `target` schema inside `catalog` (for example, `catalog`.`target`.`table`). If `target` is not specified, no data is published to Unity Catalog. |
| `effective_settings.channel` | string | DLT Release Channel that specifies which version to use. |
| `effective_settings.clusters` | array<string> | Cluster settings for this pipeline deployment. |
| `effective_settings.clusters[].apply_policy_default_values` | boolean | Note: This field won't be persisted. Only API users will check this field. |
| `effective_settings.clusters[].autoscale` | object |  |
| `effective_settings.clusters[].autoscale.max_workers` | number | The maximum number of workers to which the cluster can scale up when overloaded. `max_workers` must be strictly greater than `min_workers`. |
| `effective_settings.clusters[].autoscale.min_workers` | number | The minimum number of workers the cluster can scale down to when underutilized. It is also the initial number of workers the cluster will have after creation. |
| `effective_settings.clusters[].autoscale.mode` | string | Databricks Enhanced Autoscaling optimizes cluster utilization by automatically allocating cluster resources based on workload volume, with minimal impact to the data processing latency of your pipelines. Enhanced Autoscaling is available for `updates` clusters only. The legacy autoscaling feature is used for `maintenance` clusters. |
| `effective_settings.clusters[].aws_attributes` | object | Attributes set during cluster creation which are related to Amazon Web Services. |
| `effective_settings.clusters[].aws_attributes.availability` | string | Availability type used for all subsequent nodes past the `first_on_demand` ones.  Note: If `first_on_demand` is zero, this availability type will be used for the entire cluster. |
| `effective_settings.clusters[].aws_attributes.ebs_volume_count` | number | The number of volumes launched for each instance. Users can choose up to 10 volumes. This feature is only enabled for supported node types. Legacy node types cannot specify custom EBS volumes. For node types with no instance store, at least one EBS volume needs to be specified; otherwise, cluster creation will fail.  These EBS volumes will be mounted at `/ebs0`, `/ebs1`, and etc. Instance store volumes will be mounted at `/local_disk0`, `/local_disk1`, and etc.  If EBS volumes are attached, Databricks will configure Spark to use only the EBS volumes for scratch storage because heterogenously sized scratch devices can lead to inefficient disk utilization. If no EBS volumes are attached, Databricks will configure Spark to use instance store volumes.  Please note that if EBS volumes are specified, then the Spark configuration `spark.local.dir` will be overridden. |
| `effective_settings.clusters[].aws_attributes.ebs_volume_iops` | number | If using gp3 volumes, what IOPS to use for the disk. If this is not set, the maximum performance of a gp2 volume with the same volume size will be used. |
| `effective_settings.clusters[].aws_attributes.ebs_volume_size` | number | The size of each EBS volume (in GiB) launched for each instance. For general purpose SSD, this value must be within the range 100 - 4096. For throughput optimized HDD, this value must be within the range 500 - 4096. |
| `effective_settings.clusters[].aws_attributes.ebs_volume_throughput` | number | If using gp3 volumes, what throughput to use for the disk. If this is not set, the maximum performance of a gp2 volume with the same volume size will be used. |
| `effective_settings.clusters[].aws_attributes.ebs_volume_type` | string | All EBS volume types that Databricks supports. See https://aws.amazon.com/ebs/details/ for details. |
| `effective_settings.clusters[].aws_attributes.first_on_demand` | number | The first `first_on_demand` nodes of the cluster will be placed on on-demand instances. If this value is greater than 0, the cluster driver node in particular will be placed on an on-demand instance. If this value is greater than or equal to the current cluster size, all nodes will be placed on on-demand instances. If this value is less than the current cluster size, `first_on_demand` nodes will be placed on on-demand instances and the remainder will be placed on `availability` instances. Note that this value does not affect cluster size and cannot currently be mutated over the lifetime of a cluster. |
| `effective_settings.clusters[].aws_attributes.instance_profile_arn` | string | Nodes for this cluster will only be placed on AWS instances with this instance profile. If ommitted, nodes will be placed on instances without an IAM instance profile. The instance profile must have previously been added to the Databricks environment by an account administrator.  This feature may only be available to certain customer plans. |
| `effective_settings.clusters[].aws_attributes.spot_bid_price_percent` | number | The bid price for AWS spot instances, as a percentage of the corresponding instance type's on-demand price. For example, if this field is set to 50, and the cluster needs a new `r3.xlarge` spot instance, then the bid price is half of the price of on-demand `r3.xlarge` instances. Similarly, if this field is set to 200, the bid price is twice the price of on-demand `r3.xlarge` instances. If not specified, the default value is 100. When spot instances are requested for this cluster, only spot instances whose bid price percentage matches this field will be considered. Note that, for safety, we enforce this field to be no more than 10000. |
| `effective_settings.clusters[].aws_attributes.zone_id` | string | Identifier for the availability zone/datacenter in which the cluster resides. This string will be of a form like "us-west-2a". The provided availability zone must be in the same region as the Databricks deployment. For example, "us-west-2a" is not a valid zone id if the Databricks deployment resides in the "us-east-1" region. This is an optional field at cluster creation, and if not specified, the zone "auto" will be used. If the zone specified is "auto", will try to place cluster in a zone with high availability, and will retry placement in a different AZ if there is not enough capacity.  The list of available zones as well as the default value can be found by using the `List Zones` method. |
| `effective_settings.clusters[].cluster_log_conf` | object | Cluster log delivery config |
| `effective_settings.clusters[].cluster_log_conf.dbfs` | object | A storage location in DBFS |
| `effective_settings.clusters[].cluster_log_conf.dbfs.destination` | string | dbfs destination, e.g. `dbfs:/my/path` |
| `effective_settings.clusters[].cluster_log_conf.s3` | object | A storage location in Amazon S3 |
| `effective_settings.clusters[].cluster_log_conf.s3.canned_acl` | string | (Optional) Set canned access control list for the logs, e.g. `bucket-owner-full-control`. If `canned_cal` is set, please make sure the cluster iam role has `s3:PutObjectAcl` permission on the destination bucket and prefix. The full list of possible canned acl can be found at http://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html#canned-acl. Please also note that by default only the object owner gets full controls. If you are using cross account role for writing data, you may want to set `bucket-owner-full-control` to make bucket owner able to read the logs. |
| `effective_settings.clusters[].cluster_log_conf.s3.destination` | string | S3 destination, e.g. `s3://my-bucket/some-prefix` Note that logs will be delivered using cluster iam role, please make sure you set cluster iam role and the role has write access to the destination. Please also note that you cannot use AWS keys to deliver logs. |
| `effective_settings.clusters[].cluster_log_conf.s3.enable_encryption` | boolean | (Optional) Flag to enable server side encryption, `false` by default. |
| `effective_settings.clusters[].cluster_log_conf.s3.encryption_type` | string | (Optional) The encryption type, it could be `sse-s3` or `sse-kms`. It will be used only when encryption is enabled and the default type is `sse-s3`. |
| `effective_settings.clusters[].cluster_log_conf.s3.endpoint` | string | S3 endpoint, e.g. `https://s3-us-west-2.amazonaws.com`. Either region or endpoint needs to be set. If both are set, endpoint will be used. |
| `effective_settings.clusters[].cluster_log_conf.s3.kms_key` | string | (Optional) Kms key which will be used if encryption is enabled and encryption type is set to `sse-kms`. |
| `effective_settings.clusters[].cluster_log_conf.s3.region` | string | S3 region, e.g. `us-west-2`. Either region or endpoint needs to be set. If both are set, endpoint will be used. |
| `effective_settings.clusters[].cluster_log_conf.volumes` | object | A storage location back by UC Volumes. |
| `effective_settings.clusters[].cluster_log_conf.volumes.destination` | string | UC Volumes destination, e.g. `/Volumes/catalog/schema/vol1/init-scripts/setup-datadog.sh` or `dbfs:/Volumes/catalog/schema/vol1/init-scripts/setup-datadog.sh` |
| `effective_settings.clusters[].custom_tags` | object | Additional tags for cluster resources. Databricks will tag all cluster resources (e.g., AWS instances and EBS volumes) with these tags in addition to `default_tags`. Notes:  - Currently, Databricks allows at most 45 custom tags  - Clusters can only reuse cloud resources if the resources' tags are a subset of the cluster tags |
| `effective_settings.clusters[].driver_instance_pool_id` | string | The optional ID of the instance pool for the driver of the cluster belongs. The pool cluster uses the instance pool with id (instance_pool_id) if the driver pool is not assigned. |
| `effective_settings.clusters[].driver_node_type_id` | string | The node type of the Spark driver. Note that this field is optional; if unset, the driver node type will be set as the same value as `node_type_id` defined above. |
| `effective_settings.clusters[].enable_local_disk_encryption` | boolean | Whether to enable local disk encryption for the cluster. |
| `effective_settings.clusters[].init_scripts` | array<string> | The configuration for storing init scripts. Any number of destinations can be specified. The scripts are executed sequentially in the order provided. If `cluster_log_conf` is specified, init script logs are sent to `<destination>/<cluster-ID>/init_scripts`. |
| `effective_settings.clusters[].init_scripts[].abfss` | object | A storage location in Adls Gen2 |
| `effective_settings.clusters[].init_scripts[].abfss.destination` | string | abfss destination, e.g. `abfss://<container-name>@<storage-account-name>.dfs.core.windows.net/<directory-name>`. |
| `effective_settings.clusters[].init_scripts[].dbfs` | object | A storage location in DBFS |
| `effective_settings.clusters[].init_scripts[].dbfs.destination` | string | dbfs destination, e.g. `dbfs:/my/path` |
| `effective_settings.clusters[].init_scripts[].file` | object |  |
| `effective_settings.clusters[].init_scripts[].file.destination` | string | local file destination, e.g. `file:/my/local/file.sh` |
| `effective_settings.clusters[].init_scripts[].gcs` | object | A storage location in Google Cloud Platform's GCS |
| `effective_settings.clusters[].init_scripts[].gcs.destination` | string | GCS destination/URI, e.g. `gs://my-bucket/some-prefix` |
| `effective_settings.clusters[].init_scripts[].s3` | object | A storage location in Amazon S3 |
| `effective_settings.clusters[].init_scripts[].s3.canned_acl` | string | (Optional) Set canned access control list for the logs, e.g. `bucket-owner-full-control`. If `canned_cal` is set, please make sure the cluster iam role has `s3:PutObjectAcl` permission on the destination bucket and prefix. The full list of possible canned acl can be found at http://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html#canned-acl. Please also note that by default only the object owner gets full controls. If you are using cross account role for writing data, you may want to set `bucket-owner-full-control` to make bucket owner able to read the logs. |
| `effective_settings.clusters[].init_scripts[].s3.destination` | string | S3 destination, e.g. `s3://my-bucket/some-prefix` Note that logs will be delivered using cluster iam role, please make sure you set cluster iam role and the role has write access to the destination. Please also note that you cannot use AWS keys to deliver logs. |
| `effective_settings.clusters[].init_scripts[].s3.enable_encryption` | boolean | (Optional) Flag to enable server side encryption, `false` by default. |
| `effective_settings.clusters[].init_scripts[].s3.encryption_type` | string | (Optional) The encryption type, it could be `sse-s3` or `sse-kms`. It will be used only when encryption is enabled and the default type is `sse-s3`. |
| `effective_settings.clusters[].init_scripts[].s3.endpoint` | string | S3 endpoint, e.g. `https://s3-us-west-2.amazonaws.com`. Either region or endpoint needs to be set. If both are set, endpoint will be used. |
| `effective_settings.clusters[].init_scripts[].s3.kms_key` | string | (Optional) Kms key which will be used if encryption is enabled and encryption type is set to `sse-kms`. |
| `effective_settings.clusters[].init_scripts[].s3.region` | string | S3 region, e.g. `us-west-2`. Either region or endpoint needs to be set. If both are set, endpoint will be used. |
| `effective_settings.clusters[].init_scripts[].volumes` | object | A storage location back by UC Volumes. |
| `effective_settings.clusters[].init_scripts[].volumes.destination` | string | UC Volumes destination, e.g. `/Volumes/catalog/schema/vol1/init-scripts/setup-datadog.sh` or `dbfs:/Volumes/catalog/schema/vol1/init-scripts/setup-datadog.sh` |
| `effective_settings.clusters[].init_scripts[].workspace` | object | A storage location in Workspace Filesystem (WSFS) |
| `effective_settings.clusters[].init_scripts[].workspace.destination` | string | wsfs destination, e.g. `workspace:/cluster-init-scripts/setup-datadog.sh` |
| `effective_settings.clusters[].instance_pool_id` | string | The optional ID of the instance pool to which the cluster belongs. |
| `effective_settings.clusters[].label` | string | A label for the cluster specification, either `default` to configure the default cluster, or `maintenance` to configure the maintenance cluster. This field is optional. The default value is `default`. |
| `effective_settings.clusters[].node_type_id` | string | This field encodes, through a single value, the resources available to each of the Spark nodes in this cluster. For example, the Spark nodes can be provisioned and optimized for memory or compute intensive workloads. A list of available node types can be retrieved by using the :method:clusters/listNodeTypes API call. |
| `effective_settings.clusters[].num_workers` | number | Number of worker nodes that this cluster should have. A cluster has one Spark Driver and `num_workers` Executors for a total of `num_workers` + 1 Spark nodes.  Note: When reading the properties of a cluster, this field reflects the desired number of workers rather than the actual current number of workers. For instance, if a cluster is resized from 5 to 10 workers, this field will immediately be updated to reflect the target size of 10 workers, whereas the workers listed in `spark_info` will gradually increase from 5 to 10 as the new nodes are provisioned. |
| `effective_settings.clusters[].policy_id` | string | The ID of the cluster policy used to create the cluster if applicable. |
| `effective_settings.clusters[].spark_conf` | object | An object containing a set of optional, user-specified Spark configuration key-value pairs. See :method:clusters/create for more details. |
| `effective_settings.clusters[].spark_env_vars` | object | An object containing a set of optional, user-specified environment variable key-value pairs. Please note that key-value pair of the form (X,Y) will be exported as is (i.e., `export X='Y'`) while launching the driver and workers.  In order to specify an additional set of `SPARK_DAEMON_JAVA_OPTS`, we recommend appending them to `$SPARK_DAEMON_JAVA_OPTS` as shown in the example below. This ensures that all default databricks managed environmental variables are included as well.  Example Spark environment variables: `{"SPARK_WORKER_MEMORY": "28000m", "SPARK_LOCAL_DIRS": "/local_disk0"}` or `{"SPARK_DAEMON_JAVA_OPTS": "$SPARK_DAEMON_JAVA_OPTS -Dspark.shuffle.service.enabled=true"}` |
| `effective_settings.clusters[].ssh_public_keys` | array<string> | SSH public key contents that will be added to each Spark node in this cluster. The corresponding private keys can be used to login with the user name `ubuntu` on port `2200`. Up to 10 keys can be specified. |
| `effective_settings.configuration` | object | String-String configuration for this pipeline execution. |
| `effective_settings.continuous` | boolean | Whether the pipeline is continuous or triggered. This replaces `trigger`. |
| `effective_settings.deployment` | object |  |
| `effective_settings.deployment.kind` | string | The deployment method that manages the pipeline: - BUNDLE: The pipeline is managed by a Databricks Asset Bundle. |
| `effective_settings.deployment.metadata_file_path` | string | The path to the file containing metadata about the deployment. |
| `effective_settings.development` | boolean | Whether the pipeline is in Development mode. Defaults to false. |
| `effective_settings.edition` | string | Pipeline product edition. |
| `effective_settings.environment` | object | The environment entity used to preserve serverless environment side panel, jobs' environment for non-notebook task, and DLT's environment for classic and serverless pipelines. In this minimal environment spec, only pip dependencies are supported. |
| `effective_settings.environment.dependencies` | array<string> | List of pip dependencies, as supported by the version of pip in this environment. Each dependency is a pip requirement file line https://pip.pypa.io/en/stable/reference/requirements-file-format/ Allowed dependency could be <requirement specifier>, <archive url/path>, <local project path>(WSFS or Volumes in Databricks), <vcs project url> |
| `effective_settings.event_log` | object | Configurable event log parameters. |
| `effective_settings.event_log.catalog` | string | The UC catalog the event log is published under. |
| `effective_settings.event_log.name` | string | The name the event log is published to in UC. |
| `effective_settings.event_log.schema` | string | The UC schema the event log is published under. |
| `effective_settings.filters` | object |  |
| `effective_settings.filters.exclude` | array<string> | Paths to exclude. |
| `effective_settings.filters.include` | array<string> | Paths to include. |
| `effective_settings.id` | string | Unique identifier for this pipeline. |
| `effective_settings.ingestion_definition` | object |  |
| `effective_settings.ingestion_definition.connection_name` | string | The Unity Catalog connection that this ingestion pipeline uses to communicate with the source. This is used with both connectors for applications like Salesforce, Workday, and so on, and also database connectors like Oracle, (connector_type = QUERY_BASED OR connector_type = CDC). If connection name corresponds to database connectors like Oracle, and connector_type is not provided then connector_type defaults to QUERY_BASED. If connector_type is passed as CDC we use Combined Cdc Managed Ingestion pipeline. Under certain conditions, this can be replaced with ingestion_gateway_id to change the connector to Cdc Managed Ingestion Pipeline with Gateway pipeline. |
| `effective_settings.ingestion_definition.full_refresh_window` | object | Proto representing a window |
| `effective_settings.ingestion_definition.full_refresh_window.days_of_week` | array<string> | Days of week in which the window is allowed to happen If not specified all days of the week will be used. |
| `effective_settings.ingestion_definition.full_refresh_window.start_hour` | number | An integer between 0 and 23 denoting the start hour for the window in the 24-hour day. |
| `effective_settings.ingestion_definition.full_refresh_window.time_zone_id` | string | Time zone id of window. See https://docs.databricks.com/sql/language-manual/sql-ref-syntax-aux-conf-mgmt-set-timezone.html for details. If not specified, UTC will be used. |
| `effective_settings.ingestion_definition.ingestion_gateway_id` | string | Identifier for the gateway that is used by this ingestion pipeline to communicate with the source database. This is used with CDC connectors to databases like SQL Server using a gateway pipeline (connector_type = CDC). Under certain conditions, this can be replaced with connection_name to change the connector to Combined Cdc Managed Ingestion Pipeline. |
| `effective_settings.ingestion_definition.objects` | array<string> | Required. Settings specifying tables to replicate and the destination for the replicated tables. |
| `effective_settings.ingestion_definition.objects[].report` | object |  |
| `effective_settings.ingestion_definition.objects[].report.destination_catalog` | string | Required. Destination catalog to store table. |
| `effective_settings.ingestion_definition.objects[].report.destination_schema` | string | Required. Destination schema to store table. |
| `effective_settings.ingestion_definition.objects[].report.destination_table` | string | Required. Destination table name. The pipeline fails if a table with that name already exists. |
| `effective_settings.ingestion_definition.objects[].report.source_url` | string | Required. Report URL in the source system. |
| `effective_settings.ingestion_definition.objects[].report.table_configuration` | object |  |
| `effective_settings.ingestion_definition.objects[].schema` | object |  |
| `effective_settings.ingestion_definition.objects[].schema.destination_catalog` | string | Required. Destination catalog to store tables. |
| `effective_settings.ingestion_definition.objects[].schema.destination_schema` | string | Required. Destination schema to store tables in. Tables with the same name as the source tables are created in this destination schema. The pipeline fails If a table with the same name already exists. |
| `effective_settings.ingestion_definition.objects[].schema.source_catalog` | string | The source catalog name. Might be optional depending on the type of source. |
| `effective_settings.ingestion_definition.objects[].schema.source_schema` | string | Required. Schema name in the source database. |
| `effective_settings.ingestion_definition.objects[].schema.table_configuration` | object |  |
| `effective_settings.ingestion_definition.objects[].table` | object |  |
| `effective_settings.ingestion_definition.objects[].table.destination_catalog` | string | Required. Destination catalog to store table. |
| `effective_settings.ingestion_definition.objects[].table.destination_schema` | string | Required. Destination schema to store table. |
| `effective_settings.ingestion_definition.objects[].table.destination_table` | string | Optional. Destination table name. The pipeline fails if a table with that name already exists. If not set, the source table name is used. |
| `effective_settings.ingestion_definition.objects[].table.source_catalog` | string | Source catalog name. Might be optional depending on the type of source. |
| `effective_settings.ingestion_definition.objects[].table.source_schema` | string | Schema name in the source database. Might be optional depending on the type of source. |
| `effective_settings.ingestion_definition.objects[].table.source_table` | string | Required. Table name in the source database. |
| `effective_settings.ingestion_definition.objects[].table.table_configuration` | object |  |
| `effective_settings.ingestion_definition.source_configurations` | array<string> | Top-level source configurations |
| `effective_settings.ingestion_definition.source_configurations[].catalog` | object | SourceCatalogConfig contains catalog-level custom configuration parameters for each source |
| `effective_settings.ingestion_definition.source_configurations[].catalog.postgres` | object | PG-specific catalog-level configuration parameters |
| `effective_settings.ingestion_definition.source_configurations[].catalog.source_catalog` | string | Source catalog name |
| `effective_settings.ingestion_definition.source_type` | string |  |
| `effective_settings.ingestion_definition.table_configuration` | object |  |
| `effective_settings.ingestion_definition.table_configuration.auto_full_refresh_policy` | object | Policy for auto full refresh. |
| `effective_settings.ingestion_definition.table_configuration.auto_full_refresh_policy.enabled` | boolean | (Required, Mutable) Whether to enable auto full refresh or not. |
| `effective_settings.ingestion_definition.table_configuration.auto_full_refresh_policy.min_interval_hours` | number | (Optional, Mutable) Specify the minimum interval in hours between the timestamp at which a table was last full refreshed and the current timestamp for triggering auto full If unspecified and autoFullRefresh is enabled then by default min_interval_hours is 24 hours. |
| `effective_settings.ingestion_definition.table_configuration.exclude_columns` | array<string> | A list of column names to be excluded for the ingestion. When not specified, include_columns fully controls what columns to be ingested. When specified, all other columns including future ones will be automatically included for ingestion. This field in mutually exclusive with `include_columns`. |
| `effective_settings.ingestion_definition.table_configuration.include_columns` | array<string> | A list of column names to be included for the ingestion. When not specified, all columns except ones in exclude_columns will be included. Future columns will be automatically included. When specified, all other future columns will be automatically excluded from ingestion. This field in mutually exclusive with `exclude_columns`. |
| `effective_settings.ingestion_definition.table_configuration.primary_keys` | array<string> | The primary key of the table used to apply changes. |
| `effective_settings.ingestion_definition.table_configuration.sequence_by` | array<string> | The column names specifying the logical order of events in the source data. Spark Declarative Pipelines uses this sequencing to handle change events that arrive out of order. |
| `effective_settings.libraries` | array<string> | Libraries or code needed by this deployment. |
| `effective_settings.libraries[].file` | object |  |
| `effective_settings.libraries[].file.path` | string | The absolute path of the source code. |
| `effective_settings.libraries[].glob` | object |  |
| `effective_settings.libraries[].glob.include` | string | The source code to include for pipelines |
| `effective_settings.libraries[].notebook` | object |  |
| `effective_settings.libraries[].notebook.path` | string | The absolute path of the source code. |
| `effective_settings.libraries[].whl` | string | URI of the whl to be installed. |
| `effective_settings.name` | string | Friendly identifier for this pipeline. |
| `effective_settings.notifications` | array<string> | List of notification settings for this pipeline. |
| `effective_settings.notifications[].alerts` | array<string> | A list of alerts that trigger the sending of notifications to the configured destinations. The supported alerts are:  * `on-update-success`: A pipeline update completes successfully. * `on-update-failure`: Each time a pipeline update fails. * `on-update-fatal-failure`: A pipeline update fails with a non-retryable (fatal) error. * `on-flow-failure`: A single data flow fails. |
| `effective_settings.notifications[].email_recipients` | array<string> | A list of email addresses notified when a configured alert is triggered. |
| `effective_settings.photon` | boolean | Whether Photon is enabled for this pipeline. |
| `effective_settings.root_path` | string | Root path for this pipeline. This is used as the root directory when editing the pipeline in the Databricks user interface and it is added to sys.path when executing Python sources during pipeline execution. |
| `effective_settings.schema` | string | The default schema (database) where tables are read from or published to. |
| `effective_settings.serverless` | boolean | Whether serverless compute is enabled for this pipeline. |
| `effective_settings.storage` | string | DBFS root directory for storing checkpoints and tables. |
| `effective_settings.tags` | object | A map of tags associated with the pipeline. These are forwarded to the cluster as cluster tags, and are therefore subject to the same limitations. A maximum of 25 tags can be added to the pipeline. |
| `effective_settings.target` | string | Target schema (database) to add tables in this pipeline to. Exactly one of `schema` or `target` must be specified. To publish to Unity Catalog, also specify `catalog`. This legacy field is deprecated for pipeline creation in favor of the `schema` field. |
| `effective_settings.trigger` | object |  |
| `effective_settings.trigger.cron` | object |  |
| `effective_settings.trigger.cron.quartz_cron_schedule` | string |  |
| `effective_settings.trigger.cron.timezone_id` | string |  |
| `effective_settings.trigger.manual` | object |  |
| `pipeline_id` | string | The unique identifier for the newly created pipeline. Only returned when dry_run is false. |

## Native endpoint

Through the native Databricks API, this operation is `POST {{credentials.host}}/api/2.0/pipelines` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pipeline.md) for the provider-specific parameters and requirements.

