# Databricks: List Clusters

Retrieves clusters from the Databricks workspace.

```
GET https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-clusters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-clusters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-clusters?${params}`, {
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
| `filterBy` | object | no | Filters to apply to the list of clusters. |
| `pageToken` | string | no | Use next_page_token or prev_page_token returned from the previous request to list the next or previous page of clusters respectively. |
| `pageSize` | number | no | Use this field to specify the maximum number of results to be returned by the server. The server may further constrain the maximum number of results returned in a single page. |
| `sortBy` | object | no | Sort the list of clusters by a specific criteria. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      "cluster_cores": 1,
      "cluster_id": "string",
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
      "cluster_log_status": {
        "last_attempted": 1,
        "last_exception": "string"
      },
      "cluster_memory_mb": 1,
      "cluster_name": "Ava Chen",
      "cluster_source": "string",
      "creator_user_name": "Ava Chen",
      "custom_tags": {},
      "data_security_mode": "string",
      "default_tags": {},
      "docker_image": {
        "basic_auth": {
          "password": "string",
          "username": "Ava Chen"
        },
        "url": "https://example.com"
      },
      "driver": {
        "host_private_ip": "string",
        "instance_id": "string",
        "node_aws_attributes": {
          "is_spot": true
        },
        "node_id": "string",
        "private_ip": "string",
        "public_dns": "string",
        "start_timestamp": 1
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
      "executors": [
        {
          "host_private_ip": "string",
          "instance_id": "string",
          "node_aws_attributes": {
            "is_spot": true
          },
          "node_id": "string",
          "private_ip": "string",
          "public_dns": "string",
          "start_timestamp": 1
        }
      ],
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
      "is_single_node": true,
      "jdbc_port": 1,
      "kind": "string",
      "last_restarted_time": 1,
      "last_state_loss_time": 1,
      "node_type_id": "string",
      "num_workers": 1,
      "policy_id": "string",
      "runtime_engine": "string",
      "single_user_name": "Ava Chen",
      "spark_conf": {},
      "spark_context_id": 1,
      "spark_env_vars": {},
      "spark_version": "string",
      "spec": {
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
        "cluster_name": "Ava Chen",
        "custom_tags": {},
        "data_security_mode": "string",
        "docker_image": {
          "basic_auth": {
            "password": "string",
            "username": "Ava Chen"
          },
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
          "clients": {
            "jobs": true,
            "notebooks": true
          }
        }
      },
      "ssh_public_keys": [
        "string"
      ],
      "start_time": 1,
      "state": "string",
      "state_message": "string",
      "terminated_time": 1,
      "termination_reason": {
        "code": "string",
        "parameters": {},
        "type": "string"
      },
      "use_ml_runtime": true,
      "worker_node_type_flexibility": {
        "alternate_node_type_ids": [
          "string"
        ]
      },
      "workload_type": {
        "clients": {
          "jobs": true,
          "notebooks": true
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
| `autoscale` | object |  |
| `autoscale.max_workers` | number | The maximum number of workers to which the cluster can scale up when overloaded. Note that `max_workers` must be strictly greater than `min_workers`. |
| `autoscale.min_workers` | number | The minimum number of workers to which the cluster can scale down when underutilized. It is also the initial number of workers the cluster will have after creation. |
| `autotermination_minutes` | number | Automatically terminates the cluster after it is inactive for this time in minutes. If not set, this cluster will not be automatically terminated. If specified, the threshold must be between 10 and 10000 minutes. Users can also set this value to 0 to explicitly disable automatic termination. |
| `aws_attributes` | object | Attributes set during cluster creation which are related to Amazon Web Services. |
| `aws_attributes.availability` | string | Availability type used for all subsequent nodes past the `first_on_demand` ones.  Note: If `first_on_demand` is zero, this availability type will be used for the entire cluster. |
| `aws_attributes.ebs_volume_count` | number | The number of volumes launched for each instance. Users can choose up to 10 volumes. This feature is only enabled for supported node types. Legacy node types cannot specify custom EBS volumes. For node types with no instance store, at least one EBS volume needs to be specified; otherwise, cluster creation will fail.  These EBS volumes will be mounted at `/ebs0`, `/ebs1`, and etc. Instance store volumes will be mounted at `/local_disk0`, `/local_disk1`, and etc.  If EBS volumes are attached, Databricks will configure Spark to use only the EBS volumes for scratch storage because heterogenously sized scratch devices can lead to inefficient disk utilization. If no EBS volumes are attached, Databricks will configure Spark to use instance store volumes.  Please note that if EBS volumes are specified, then the Spark configuration `spark.local.dir` will be overridden. |
| `aws_attributes.ebs_volume_iops` | number | If using gp3 volumes, what IOPS to use for the disk. If this is not set, the maximum performance of a gp2 volume with the same volume size will be used. |
| `aws_attributes.ebs_volume_size` | number | The size of each EBS volume (in GiB) launched for each instance. For general purpose SSD, this value must be within the range 100 - 4096. For throughput optimized HDD, this value must be within the range 500 - 4096. |
| `aws_attributes.ebs_volume_throughput` | number | If using gp3 volumes, what throughput to use for the disk. If this is not set, the maximum performance of a gp2 volume with the same volume size will be used. |
| `aws_attributes.ebs_volume_type` | string | All EBS volume types that Databricks supports. See https://aws.amazon.com/ebs/details/ for details. |
| `aws_attributes.first_on_demand` | number | The first `first_on_demand` nodes of the cluster will be placed on on-demand instances. If this value is greater than 0, the cluster driver node in particular will be placed on an on-demand instance. If this value is greater than or equal to the current cluster size, all nodes will be placed on on-demand instances. If this value is less than the current cluster size, `first_on_demand` nodes will be placed on on-demand instances and the remainder will be placed on `availability` instances. Note that this value does not affect cluster size and cannot currently be mutated over the lifetime of a cluster. |
| `aws_attributes.instance_profile_arn` | string | Nodes for this cluster will only be placed on AWS instances with this instance profile. If ommitted, nodes will be placed on instances without an IAM instance profile. The instance profile must have previously been added to the Databricks environment by an account administrator.  This feature may only be available to certain customer plans. |
| `aws_attributes.spot_bid_price_percent` | number | The bid price for AWS spot instances, as a percentage of the corresponding instance type's on-demand price. For example, if this field is set to 50, and the cluster needs a new `r3.xlarge` spot instance, then the bid price is half of the price of on-demand `r3.xlarge` instances. Similarly, if this field is set to 200, the bid price is twice the price of on-demand `r3.xlarge` instances. If not specified, the default value is 100. When spot instances are requested for this cluster, only spot instances whose bid price percentage matches this field will be considered. Note that, for safety, we enforce this field to be no more than 10000. |
| `aws_attributes.zone_id` | string | Identifier for the availability zone/datacenter in which the cluster resides. This string will be of a form like "us-west-2a". The provided availability zone must be in the same region as the Databricks deployment. For example, "us-west-2a" is not a valid zone id if the Databricks deployment resides in the "us-east-1" region. This is an optional field at cluster creation, and if not specified, the zone "auto" will be used. If the zone specified is "auto", will try to place cluster in a zone with high availability, and will retry placement in a different AZ if there is not enough capacity.  The list of available zones as well as the default value can be found by using the `List Zones` method. |
| `cluster_cores` | number | Number of CPU cores available for this cluster. Note that this can be fractional, e.g. 7.5 cores, since certain node types are configured to share cores between Spark nodes on the same instance. |
| `cluster_id` | string | Canonical identifier for the cluster. This id is retained during cluster restarts and resizes, while each new cluster has a globally unique id. |
| `cluster_log_conf` | object | Cluster log delivery config |
| `cluster_log_conf.dbfs` | object | A storage location in DBFS |
| `cluster_log_conf.dbfs.destination` | string | dbfs destination, e.g. `dbfs:/my/path` |
| `cluster_log_conf.s3` | object | A storage location in Amazon S3 |
| `cluster_log_conf.s3.canned_acl` | string | (Optional) Set canned access control list for the logs, e.g. `bucket-owner-full-control`. If `canned_cal` is set, please make sure the cluster iam role has `s3:PutObjectAcl` permission on the destination bucket and prefix. The full list of possible canned acl can be found at http://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html#canned-acl. Please also note that by default only the object owner gets full controls. If you are using cross account role for writing data, you may want to set `bucket-owner-full-control` to make bucket owner able to read the logs. |
| `cluster_log_conf.s3.destination` | string | S3 destination, e.g. `s3://my-bucket/some-prefix` Note that logs will be delivered using cluster iam role, please make sure you set cluster iam role and the role has write access to the destination. Please also note that you cannot use AWS keys to deliver logs. |
| `cluster_log_conf.s3.enable_encryption` | boolean | (Optional) Flag to enable server side encryption, `false` by default. |
| `cluster_log_conf.s3.encryption_type` | string | (Optional) The encryption type, it could be `sse-s3` or `sse-kms`. It will be used only when encryption is enabled and the default type is `sse-s3`. |
| `cluster_log_conf.s3.endpoint` | string | S3 endpoint, e.g. `https://s3-us-west-2.amazonaws.com`. Either region or endpoint needs to be set. If both are set, endpoint will be used. |
| `cluster_log_conf.s3.kms_key` | string | (Optional) Kms key which will be used if encryption is enabled and encryption type is set to `sse-kms`. |
| `cluster_log_conf.s3.region` | string | S3 region, e.g. `us-west-2`. Either region or endpoint needs to be set. If both are set, endpoint will be used. |
| `cluster_log_conf.volumes` | object | A storage location back by UC Volumes. |
| `cluster_log_conf.volumes.destination` | string | UC Volumes destination, e.g. `/Volumes/catalog/schema/vol1/init-scripts/setup-datadog.sh` or `dbfs:/Volumes/catalog/schema/vol1/init-scripts/setup-datadog.sh` |
| `cluster_log_status` | object | The log delivery status |
| `cluster_log_status.last_attempted` | number | The timestamp of last attempt. If the last attempt fails, `last_exception` will contain the exception in the last attempt. |
| `cluster_log_status.last_exception` | string | The exception thrown in the last attempt, it would be null (omitted in the response) if there is no exception in last attempted. |
| `cluster_memory_mb` | number | Total amount of cluster memory, in megabytes |
| `cluster_name` | string | Cluster name requested by the user. This doesn't have to be unique. If not specified at creation, the cluster name will be an empty string. For job clusters, the cluster name is automatically set based on the job and job run IDs. |
| `cluster_source` | string | Determines whether the cluster was created by a user through the UI, created by the Databricks Jobs Scheduler, or through an API request. This is the same as cluster_creator, but read only. |
| `creator_user_name` | string | Creator user name. The field won't be included in the response if the user has already been deleted. |
| `custom_tags` | object | Additional tags for cluster resources. Databricks will tag all cluster resources (e.g., AWS instances and EBS volumes) with these tags in addition to `default_tags`. Notes:  - Currently, Databricks allows at most 45 custom tags  - Clusters can only reuse cloud resources if the resources' tags are a subset of the cluster tags |
| `data_security_mode` | string | Data security mode decides what data governance model to use when accessing data from a cluster.  The following modes can only be used when `kind = CLASSIC_PREVIEW`. * `DATA_SECURITY_MODE_AUTO`: Databricks will choose the most appropriate access mode depending on your compute configuration. * `DATA_SECURITY_MODE_STANDARD`: Alias for `USER_ISOLATION`. * `DATA_SECURITY_MODE_DEDICATED`: Alias for `SINGLE_USER`.  The following modes can be used regardless of `kind`. * `NONE`: No security isolation for multiple users sharing the cluster. Data governance features are not available in this mode. * `SINGLE_USER`: A secure cluster that can only be exclusively used by a single user specified in `single_user_name`. Most programming languages, cluster features and data governance features are available in this mode. * `USER_ISOLATION`: A secure cluster that can be shared by multiple users. Cluster users are fully isolated so that they cannot see each other's data and credentials. Most data governance features are supported in this mode. But programming languages and cluster features might be limited.  The following modes are deprecated starting with Databricks Runtime 15.0 and will be removed for future Databricks Runtime versions:  * `LEGACY_TABLE_ACL`: This mode is for users migrating from legacy Table ACL clusters. * `LEGACY_PASSTHROUGH`: This mode is for users migrating from legacy Passthrough on high concurrency clusters. * `LEGACY_SINGLE_USER`: This mode is for users migrating from legacy Passthrough on standard clusters. * `LEGACY_SINGLE_USER_STANDARD`: This mode provides a way that doesnât have UC nor passthrough enabled. |
| `default_tags` | object | Tags that are added by Databricks regardless of any `custom_tags`, including:  - Vendor: Databricks  - Creator: <username_of_creator>  - ClusterName: <name_of_cluster>  - ClusterId: <id_of_cluster>  - Name: <Databricks internal use> |
| `docker_image` | object |  |
| `docker_image.basic_auth` | object |  |
| `docker_image.basic_auth.password` | string | Password of the user |
| `docker_image.basic_auth.username` | string | Name of the user |
| `docker_image.url` | string | URL of the docker image. |
| `driver` | object | Describes a specific Spark driver or executor. |
| `driver_instance_pool_id` | string | The optional ID of the instance pool for the driver of the cluster belongs. The pool cluster uses the instance pool with id (instance_pool_id) if the driver pool is not assigned. |
| `driver_node_type_flexibility` | object | Configuration for flexible node types, allowing fallback to alternate node types during cluster launch and upscale. |
| `driver_node_type_flexibility.alternate_node_type_ids` | array<string> | A list of node type IDs to use as fallbacks when the primary node type is unavailable. |
| `driver_node_type_id` | string | The node type of the Spark driver. Note that this field is optional; if unset, the driver node type will be set as the same value as `node_type_id` defined above.  This field, along with node_type_id, should not be set if virtual_cluster_size is set. If both driver_node_type_id, node_type_id, and virtual_cluster_size are specified, driver_node_type_id and node_type_id take precedence. |
| `driver.host_private_ip` | string | The private IP address of the host instance. |
| `driver.instance_id` | string | Globally unique identifier for the host instance from the cloud provider. |
| `driver.node_aws_attributes` | object | Attributes specific to AWS for a Spark node. |
| `driver.node_aws_attributes.is_spot` | boolean | Whether this node is on an Amazon spot instance. |
| `driver.node_id` | string | Globally unique identifier for this node. |
| `driver.private_ip` | string | Private IP address (typically a 10.x.x.x address) of the Spark node. Note that this is different from the private IP address of the host instance. |
| `driver.public_dns` | string | Public DNS address of this node. This address can be used to access the Spark JDBC server on the driver node. To communicate with the JDBC server, traffic must be manually authorized by adding security group rules to the "worker-unmanaged" security group via the AWS console. |
| `driver.start_timestamp` | number | The timestamp (in millisecond) when the Spark node is launched. |
| `enable_elastic_disk` | boolean | Autoscaling Local Storage: when enabled, this cluster will dynamically acquire additional disk space when its Spark workers are running low on disk space.  This feature requires specific AWS permissions to function correctly - refer to the User Guide for more details. |
| `enable_local_disk_encryption` | boolean | Whether to enable LUKS on cluster VMs' local disks |
| `executors` | array<string> | Nodes on which the Spark executors reside. |
| `executors[].host_private_ip` | string | The private IP address of the host instance. |
| `executors[].instance_id` | string | Globally unique identifier for the host instance from the cloud provider. |
| `executors[].node_aws_attributes` | object | Attributes specific to AWS for a Spark node. |
| `executors[].node_aws_attributes.is_spot` | boolean | Whether this node is on an Amazon spot instance. |
| `executors[].node_id` | string | Globally unique identifier for this node. |
| `executors[].private_ip` | string | Private IP address (typically a 10.x.x.x address) of the Spark node. Note that this is different from the private IP address of the host instance. |
| `executors[].public_dns` | string | Public DNS address of this node. This address can be used to access the Spark JDBC server on the driver node. To communicate with the JDBC server, traffic must be manually authorized by adding security group rules to the "worker-unmanaged" security group via the AWS console. |
| `executors[].start_timestamp` | number | The timestamp (in millisecond) when the Spark node is launched. |
| `init_scripts` | array<string> | The configuration for storing init scripts. Any number of destinations can be specified. The scripts are executed sequentially in the order provided. If `cluster_log_conf` is specified, init script logs are sent to `<destination>/<cluster-ID>/init_scripts`. |
| `init_scripts[].abfss` | object | A storage location in Adls Gen2 |
| `init_scripts[].abfss.destination` | string | abfss destination, e.g. `abfss://<container-name>@<storage-account-name>.dfs.core.windows.net/<directory-name>`. |
| `init_scripts[].dbfs` | object | A storage location in DBFS |
| `init_scripts[].dbfs.destination` | string | dbfs destination, e.g. `dbfs:/my/path` |
| `init_scripts[].file` | object |  |
| `init_scripts[].file.destination` | string | local file destination, e.g. `file:/my/local/file.sh` |
| `init_scripts[].gcs` | object | A storage location in Google Cloud Platform's GCS |
| `init_scripts[].gcs.destination` | string | GCS destination/URI, e.g. `gs://my-bucket/some-prefix` |
| `init_scripts[].s3` | object | A storage location in Amazon S3 |
| `init_scripts[].s3.canned_acl` | string | (Optional) Set canned access control list for the logs, e.g. `bucket-owner-full-control`. If `canned_cal` is set, please make sure the cluster iam role has `s3:PutObjectAcl` permission on the destination bucket and prefix. The full list of possible canned acl can be found at http://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html#canned-acl. Please also note that by default only the object owner gets full controls. If you are using cross account role for writing data, you may want to set `bucket-owner-full-control` to make bucket owner able to read the logs. |
| `init_scripts[].s3.destination` | string | S3 destination, e.g. `s3://my-bucket/some-prefix` Note that logs will be delivered using cluster iam role, please make sure you set cluster iam role and the role has write access to the destination. Please also note that you cannot use AWS keys to deliver logs. |
| `init_scripts[].s3.enable_encryption` | boolean | (Optional) Flag to enable server side encryption, `false` by default. |
| `init_scripts[].s3.encryption_type` | string | (Optional) The encryption type, it could be `sse-s3` or `sse-kms`. It will be used only when encryption is enabled and the default type is `sse-s3`. |
| `init_scripts[].s3.endpoint` | string | S3 endpoint, e.g. `https://s3-us-west-2.amazonaws.com`. Either region or endpoint needs to be set. If both are set, endpoint will be used. |
| `init_scripts[].s3.kms_key` | string | (Optional) Kms key which will be used if encryption is enabled and encryption type is set to `sse-kms`. |
| `init_scripts[].s3.region` | string | S3 region, e.g. `us-west-2`. Either region or endpoint needs to be set. If both are set, endpoint will be used. |
| `init_scripts[].volumes` | object | A storage location back by UC Volumes. |
| `init_scripts[].volumes.destination` | string | UC Volumes destination, e.g. `/Volumes/catalog/schema/vol1/init-scripts/setup-datadog.sh` or `dbfs:/Volumes/catalog/schema/vol1/init-scripts/setup-datadog.sh` |
| `init_scripts[].workspace` | object | A storage location in Workspace Filesystem (WSFS) |
| `init_scripts[].workspace.destination` | string | wsfs destination, e.g. `workspace:/cluster-init-scripts/setup-datadog.sh` |
| `instance_pool_id` | string | The optional ID of the instance pool to which the cluster belongs. |
| `is_single_node` | boolean | This field can only be used when `kind = CLASSIC_PREVIEW`.  When set to true, Databricks will automatically set single node related `custom_tags`, `spark_conf`, and `num_workers` |
| `jdbc_port` | number | Port on which Spark JDBC server is listening, in the driver nod. No service will be listeningon on this port in executor nodes. |
| `kind` | string | The kind of compute described by this compute specification.  Depending on `kind`, different validations and default values will be applied.  Clusters with `kind = CLASSIC_PREVIEW` support the following fields, whereas clusters with no specified `kind` do not. * [is_single_node](/api/workspace/clusters/create#is_single_node) * [use_ml_runtime](/api/workspace/clusters/create#use_ml_runtime) * [data_security_mode](/api/workspace/clusters/create#data_security_mode) set to `DATA_SECURITY_MODE_AUTO`, `DATA_SECURITY_MODE_DEDICATED`, or `DATA_SECURITY_MODE_STANDARD`  By using the [simple form](https://docs.databricks.com/compute/simple-form.html), your clusters are automatically using `kind = CLASSIC_PREVIEW`. |
| `last_restarted_time` | number | the timestamp that the cluster was started/restarted |
| `last_state_loss_time` | number | Time when the cluster driver last lost its state (due to a restart or driver failure). |
| `node_type_id` | string | This field encodes, through a single value, the resources available to each of the Spark nodes in this cluster. For example, the Spark nodes can be provisioned and optimized for memory or compute intensive workloads. A list of available node types can be retrieved by using the :method:clusters/listNodeTypes API call. |
| `num_workers` | number | Number of worker nodes that this cluster should have. A cluster has one Spark Driver and `num_workers` Executors for a total of `num_workers` + 1 Spark nodes.  Note: When reading the properties of a cluster, this field reflects the desired number of workers rather than the actual current number of workers. For instance, if a cluster is resized from 5 to 10 workers, this field will immediately be updated to reflect the target size of 10 workers, whereas the workers listed in `spark_info` will gradually increase from 5 to 10 as the new nodes are provisioned. |
| `policy_id` | string | The ID of the cluster policy used to create the cluster if applicable. |
| `runtime_engine` | string |  |
| `single_user_name` | string | Single user name if data_security_mode is `SINGLE_USER` |
| `spark_conf` | object | An object containing a set of optional, user-specified Spark configuration key-value pairs. Users can also pass in a string of extra JVM options to the driver and the executors via `spark.driver.extraJavaOptions` and `spark.executor.extraJavaOptions` respectively. |
| `spark_context_id` | number | A canonical SparkContext identifier. This value *does* change when the Spark driver restarts. The pair `(cluster_id, spark_context_id)` is a globally unique identifier over all Spark contexts. |
| `spark_env_vars` | object | An object containing a set of optional, user-specified environment variable key-value pairs. Please note that key-value pair of the form (X,Y) will be exported as is (i.e., `export X='Y'`) while launching the driver and workers.  In order to specify an additional set of `SPARK_DAEMON_JAVA_OPTS`, we recommend appending them to `$SPARK_DAEMON_JAVA_OPTS` as shown in the example below. This ensures that all default databricks managed environmental variables are included as well.  Example Spark environment variables: `{"SPARK_WORKER_MEMORY": "28000m", "SPARK_LOCAL_DIRS": "/local_disk0"}` or `{"SPARK_DAEMON_JAVA_OPTS": "$SPARK_DAEMON_JAVA_OPTS -Dspark.shuffle.service.enabled=true"}` |
| `spark_version` | string | The Spark version of the cluster, e.g. `3.3.x-scala2.11`. A list of available Spark versions can be retrieved by using the :method:clusters/sparkVersions API call. |
| `spec` | object | Contains a snapshot of the latest user specified settings that were used to create/edit the cluster. |
| `spec.apply_policy_default_values` | boolean | When set to true, fixed and default values from the policy will be used for fields that are omitted. When set to false, only fixed values from the policy will be applied. |
| `spec.autoscale` | object |  |
| `spec.autoscale.max_workers` | number | The maximum number of workers to which the cluster can scale up when overloaded. Note that `max_workers` must be strictly greater than `min_workers`. |
| `spec.autoscale.min_workers` | number | The minimum number of workers to which the cluster can scale down when underutilized. It is also the initial number of workers the cluster will have after creation. |
| `spec.autotermination_minutes` | number | Automatically terminates the cluster after it is inactive for this time in minutes. If not set, this cluster will not be automatically terminated. If specified, the threshold must be between 10 and 10000 minutes. Users can also set this value to 0 to explicitly disable automatic termination. |
| `spec.aws_attributes` | object | Attributes set during cluster creation which are related to Amazon Web Services. |
| `spec.aws_attributes.availability` | string | Availability type used for all subsequent nodes past the `first_on_demand` ones.  Note: If `first_on_demand` is zero, this availability type will be used for the entire cluster. |
| `spec.aws_attributes.ebs_volume_count` | number | The number of volumes launched for each instance. Users can choose up to 10 volumes. This feature is only enabled for supported node types. Legacy node types cannot specify custom EBS volumes. For node types with no instance store, at least one EBS volume needs to be specified; otherwise, cluster creation will fail.  These EBS volumes will be mounted at `/ebs0`, `/ebs1`, and etc. Instance store volumes will be mounted at `/local_disk0`, `/local_disk1`, and etc.  If EBS volumes are attached, Databricks will configure Spark to use only the EBS volumes for scratch storage because heterogenously sized scratch devices can lead to inefficient disk utilization. If no EBS volumes are attached, Databricks will configure Spark to use instance store volumes.  Please note that if EBS volumes are specified, then the Spark configuration `spark.local.dir` will be overridden. |
| `spec.aws_attributes.ebs_volume_iops` | number | If using gp3 volumes, what IOPS to use for the disk. If this is not set, the maximum performance of a gp2 volume with the same volume size will be used. |
| `spec.aws_attributes.ebs_volume_size` | number | The size of each EBS volume (in GiB) launched for each instance. For general purpose SSD, this value must be within the range 100 - 4096. For throughput optimized HDD, this value must be within the range 500 - 4096. |
| `spec.aws_attributes.ebs_volume_throughput` | number | If using gp3 volumes, what throughput to use for the disk. If this is not set, the maximum performance of a gp2 volume with the same volume size will be used. |
| `spec.aws_attributes.ebs_volume_type` | string | All EBS volume types that Databricks supports. See https://aws.amazon.com/ebs/details/ for details. |
| `spec.aws_attributes.first_on_demand` | number | The first `first_on_demand` nodes of the cluster will be placed on on-demand instances. If this value is greater than 0, the cluster driver node in particular will be placed on an on-demand instance. If this value is greater than or equal to the current cluster size, all nodes will be placed on on-demand instances. If this value is less than the current cluster size, `first_on_demand` nodes will be placed on on-demand instances and the remainder will be placed on `availability` instances. Note that this value does not affect cluster size and cannot currently be mutated over the lifetime of a cluster. |
| `spec.aws_attributes.instance_profile_arn` | string | Nodes for this cluster will only be placed on AWS instances with this instance profile. If ommitted, nodes will be placed on instances without an IAM instance profile. The instance profile must have previously been added to the Databricks environment by an account administrator.  This feature may only be available to certain customer plans. |
| `spec.aws_attributes.spot_bid_price_percent` | number | The bid price for AWS spot instances, as a percentage of the corresponding instance type's on-demand price. For example, if this field is set to 50, and the cluster needs a new `r3.xlarge` spot instance, then the bid price is half of the price of on-demand `r3.xlarge` instances. Similarly, if this field is set to 200, the bid price is twice the price of on-demand `r3.xlarge` instances. If not specified, the default value is 100. When spot instances are requested for this cluster, only spot instances whose bid price percentage matches this field will be considered. Note that, for safety, we enforce this field to be no more than 10000. |
| `spec.aws_attributes.zone_id` | string | Identifier for the availability zone/datacenter in which the cluster resides. This string will be of a form like "us-west-2a". The provided availability zone must be in the same region as the Databricks deployment. For example, "us-west-2a" is not a valid zone id if the Databricks deployment resides in the "us-east-1" region. This is an optional field at cluster creation, and if not specified, the zone "auto" will be used. If the zone specified is "auto", will try to place cluster in a zone with high availability, and will retry placement in a different AZ if there is not enough capacity.  The list of available zones as well as the default value can be found by using the `List Zones` method. |
| `spec.cluster_log_conf` | object | Cluster log delivery config |
| `spec.cluster_log_conf.dbfs` | object | A storage location in DBFS |
| `spec.cluster_log_conf.dbfs.destination` | string | dbfs destination, e.g. `dbfs:/my/path` |
| `spec.cluster_log_conf.s3` | object | A storage location in Amazon S3 |
| `spec.cluster_log_conf.s3.canned_acl` | string | (Optional) Set canned access control list for the logs, e.g. `bucket-owner-full-control`. If `canned_cal` is set, please make sure the cluster iam role has `s3:PutObjectAcl` permission on the destination bucket and prefix. The full list of possible canned acl can be found at http://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html#canned-acl. Please also note that by default only the object owner gets full controls. If you are using cross account role for writing data, you may want to set `bucket-owner-full-control` to make bucket owner able to read the logs. |
| `spec.cluster_log_conf.s3.destination` | string | S3 destination, e.g. `s3://my-bucket/some-prefix` Note that logs will be delivered using cluster iam role, please make sure you set cluster iam role and the role has write access to the destination. Please also note that you cannot use AWS keys to deliver logs. |
| `spec.cluster_log_conf.s3.enable_encryption` | boolean | (Optional) Flag to enable server side encryption, `false` by default. |
| `spec.cluster_log_conf.s3.encryption_type` | string | (Optional) The encryption type, it could be `sse-s3` or `sse-kms`. It will be used only when encryption is enabled and the default type is `sse-s3`. |
| `spec.cluster_log_conf.s3.endpoint` | string | S3 endpoint, e.g. `https://s3-us-west-2.amazonaws.com`. Either region or endpoint needs to be set. If both are set, endpoint will be used. |
| `spec.cluster_log_conf.s3.kms_key` | string | (Optional) Kms key which will be used if encryption is enabled and encryption type is set to `sse-kms`. |
| `spec.cluster_log_conf.s3.region` | string | S3 region, e.g. `us-west-2`. Either region or endpoint needs to be set. If both are set, endpoint will be used. |
| `spec.cluster_log_conf.volumes` | object | A storage location back by UC Volumes. |
| `spec.cluster_log_conf.volumes.destination` | string | UC Volumes destination, e.g. `/Volumes/catalog/schema/vol1/init-scripts/setup-datadog.sh` or `dbfs:/Volumes/catalog/schema/vol1/init-scripts/setup-datadog.sh` |
| `spec.cluster_name` | string | Cluster name requested by the user. This doesn't have to be unique. If not specified at creation, the cluster name will be an empty string. For job clusters, the cluster name is automatically set based on the job and job run IDs. |
| `spec.custom_tags` | object | Additional tags for cluster resources. Databricks will tag all cluster resources (e.g., AWS instances and EBS volumes) with these tags in addition to `default_tags`. Notes:  - Currently, Databricks allows at most 45 custom tags  - Clusters can only reuse cloud resources if the resources' tags are a subset of the cluster tags |
| `spec.data_security_mode` | string | Data security mode decides what data governance model to use when accessing data from a cluster.  The following modes can only be used when `kind = CLASSIC_PREVIEW`. * `DATA_SECURITY_MODE_AUTO`: Databricks will choose the most appropriate access mode depending on your compute configuration. * `DATA_SECURITY_MODE_STANDARD`: Alias for `USER_ISOLATION`. * `DATA_SECURITY_MODE_DEDICATED`: Alias for `SINGLE_USER`.  The following modes can be used regardless of `kind`. * `NONE`: No security isolation for multiple users sharing the cluster. Data governance features are not available in this mode. * `SINGLE_USER`: A secure cluster that can only be exclusively used by a single user specified in `single_user_name`. Most programming languages, cluster features and data governance features are available in this mode. * `USER_ISOLATION`: A secure cluster that can be shared by multiple users. Cluster users are fully isolated so that they cannot see each other's data and credentials. Most data governance features are supported in this mode. But programming languages and cluster features might be limited.  The following modes are deprecated starting with Databricks Runtime 15.0 and will be removed for future Databricks Runtime versions:  * `LEGACY_TABLE_ACL`: This mode is for users migrating from legacy Table ACL clusters. * `LEGACY_PASSTHROUGH`: This mode is for users migrating from legacy Passthrough on high concurrency clusters. * `LEGACY_SINGLE_USER`: This mode is for users migrating from legacy Passthrough on standard clusters. * `LEGACY_SINGLE_USER_STANDARD`: This mode provides a way that doesnât have UC nor passthrough enabled. |
| `spec.docker_image` | object |  |
| `spec.docker_image.basic_auth` | object |  |
| `spec.docker_image.basic_auth.password` | string | Password of the user |
| `spec.docker_image.basic_auth.username` | string | Name of the user |
| `spec.docker_image.url` | string | URL of the docker image. |
| `spec.driver_instance_pool_id` | string | The optional ID of the instance pool for the driver of the cluster belongs. The pool cluster uses the instance pool with id (instance_pool_id) if the driver pool is not assigned. |
| `spec.driver_node_type_flexibility` | object | Configuration for flexible node types, allowing fallback to alternate node types during cluster launch and upscale. |
| `spec.driver_node_type_flexibility.alternate_node_type_ids` | array<string> | A list of node type IDs to use as fallbacks when the primary node type is unavailable. |
| `spec.driver_node_type_id` | string | The node type of the Spark driver. Note that this field is optional; if unset, the driver node type will be set as the same value as `node_type_id` defined above.  This field, along with node_type_id, should not be set if virtual_cluster_size is set. If both driver_node_type_id, node_type_id, and virtual_cluster_size are specified, driver_node_type_id and node_type_id take precedence. |
| `spec.enable_elastic_disk` | boolean | Autoscaling Local Storage: when enabled, this cluster will dynamically acquire additional disk space when its Spark workers are running low on disk space.  This feature requires specific AWS permissions to function correctly - refer to the User Guide for more details. |
| `spec.enable_local_disk_encryption` | boolean | Whether to enable LUKS on cluster VMs' local disks |
| `spec.init_scripts` | array<string> | The configuration for storing init scripts. Any number of destinations can be specified. The scripts are executed sequentially in the order provided. If `cluster_log_conf` is specified, init script logs are sent to `<destination>/<cluster-ID>/init_scripts`. |
| `spec.init_scripts[].abfss` | object | A storage location in Adls Gen2 |
| `spec.init_scripts[].abfss.destination` | string | abfss destination, e.g. `abfss://<container-name>@<storage-account-name>.dfs.core.windows.net/<directory-name>`. |
| `spec.init_scripts[].dbfs` | object | A storage location in DBFS |
| `spec.init_scripts[].dbfs.destination` | string | dbfs destination, e.g. `dbfs:/my/path` |
| `spec.init_scripts[].file` | object |  |
| `spec.init_scripts[].file.destination` | string | local file destination, e.g. `file:/my/local/file.sh` |
| `spec.init_scripts[].gcs` | object | A storage location in Google Cloud Platform's GCS |
| `spec.init_scripts[].gcs.destination` | string | GCS destination/URI, e.g. `gs://my-bucket/some-prefix` |
| `spec.init_scripts[].s3` | object | A storage location in Amazon S3 |
| `spec.init_scripts[].s3.canned_acl` | string | (Optional) Set canned access control list for the logs, e.g. `bucket-owner-full-control`. If `canned_cal` is set, please make sure the cluster iam role has `s3:PutObjectAcl` permission on the destination bucket and prefix. The full list of possible canned acl can be found at http://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html#canned-acl. Please also note that by default only the object owner gets full controls. If you are using cross account role for writing data, you may want to set `bucket-owner-full-control` to make bucket owner able to read the logs. |
| `spec.init_scripts[].s3.destination` | string | S3 destination, e.g. `s3://my-bucket/some-prefix` Note that logs will be delivered using cluster iam role, please make sure you set cluster iam role and the role has write access to the destination. Please also note that you cannot use AWS keys to deliver logs. |
| `spec.init_scripts[].s3.enable_encryption` | boolean | (Optional) Flag to enable server side encryption, `false` by default. |
| `spec.init_scripts[].s3.encryption_type` | string | (Optional) The encryption type, it could be `sse-s3` or `sse-kms`. It will be used only when encryption is enabled and the default type is `sse-s3`. |
| `spec.init_scripts[].s3.endpoint` | string | S3 endpoint, e.g. `https://s3-us-west-2.amazonaws.com`. Either region or endpoint needs to be set. If both are set, endpoint will be used. |
| `spec.init_scripts[].s3.kms_key` | string | (Optional) Kms key which will be used if encryption is enabled and encryption type is set to `sse-kms`. |
| `spec.init_scripts[].s3.region` | string | S3 region, e.g. `us-west-2`. Either region or endpoint needs to be set. If both are set, endpoint will be used. |
| `spec.init_scripts[].volumes` | object | A storage location back by UC Volumes. |
| `spec.init_scripts[].volumes.destination` | string | UC Volumes destination, e.g. `/Volumes/catalog/schema/vol1/init-scripts/setup-datadog.sh` or `dbfs:/Volumes/catalog/schema/vol1/init-scripts/setup-datadog.sh` |
| `spec.init_scripts[].workspace` | object | A storage location in Workspace Filesystem (WSFS) |
| `spec.init_scripts[].workspace.destination` | string | wsfs destination, e.g. `workspace:/cluster-init-scripts/setup-datadog.sh` |
| `spec.instance_pool_id` | string | The optional ID of the instance pool to which the cluster belongs. |
| `spec.is_single_node` | boolean | This field can only be used when `kind = CLASSIC_PREVIEW`.  When set to true, Databricks will automatically set single node related `custom_tags`, `spark_conf`, and `num_workers` |
| `spec.kind` | string | The kind of compute described by this compute specification.  Depending on `kind`, different validations and default values will be applied.  Clusters with `kind = CLASSIC_PREVIEW` support the following fields, whereas clusters with no specified `kind` do not. * [is_single_node](/api/workspace/clusters/create#is_single_node) * [use_ml_runtime](/api/workspace/clusters/create#use_ml_runtime) * [data_security_mode](/api/workspace/clusters/create#data_security_mode) set to `DATA_SECURITY_MODE_AUTO`, `DATA_SECURITY_MODE_DEDICATED`, or `DATA_SECURITY_MODE_STANDARD`  By using the [simple form](https://docs.databricks.com/compute/simple-form.html), your clusters are automatically using `kind = CLASSIC_PREVIEW`. |
| `spec.node_type_id` | string | This field encodes, through a single value, the resources available to each of the Spark nodes in this cluster. For example, the Spark nodes can be provisioned and optimized for memory or compute intensive workloads. A list of available node types can be retrieved by using the :method:clusters/listNodeTypes API call. |
| `spec.num_workers` | number | Number of worker nodes that this cluster should have. A cluster has one Spark Driver and `num_workers` Executors for a total of `num_workers` + 1 Spark nodes.  Note: When reading the properties of a cluster, this field reflects the desired number of workers rather than the actual current number of workers. For instance, if a cluster is resized from 5 to 10 workers, this field will immediately be updated to reflect the target size of 10 workers, whereas the workers listed in `spark_info` will gradually increase from 5 to 10 as the new nodes are provisioned. |
| `spec.policy_id` | string | The ID of the cluster policy used to create the cluster if applicable. |
| `spec.runtime_engine` | string |  |
| `spec.single_user_name` | string | Single user name if data_security_mode is `SINGLE_USER` |
| `spec.spark_conf` | object | An object containing a set of optional, user-specified Spark configuration key-value pairs. Users can also pass in a string of extra JVM options to the driver and the executors via `spark.driver.extraJavaOptions` and `spark.executor.extraJavaOptions` respectively. |
| `spec.spark_env_vars` | object | An object containing a set of optional, user-specified environment variable key-value pairs. Please note that key-value pair of the form (X,Y) will be exported as is (i.e., `export X='Y'`) while launching the driver and workers.  In order to specify an additional set of `SPARK_DAEMON_JAVA_OPTS`, we recommend appending them to `$SPARK_DAEMON_JAVA_OPTS` as shown in the example below. This ensures that all default databricks managed environmental variables are included as well.  Example Spark environment variables: `{"SPARK_WORKER_MEMORY": "28000m", "SPARK_LOCAL_DIRS": "/local_disk0"}` or `{"SPARK_DAEMON_JAVA_OPTS": "$SPARK_DAEMON_JAVA_OPTS -Dspark.shuffle.service.enabled=true"}` |
| `spec.spark_version` | string | The Spark version of the cluster, e.g. `3.3.x-scala2.11`. A list of available Spark versions can be retrieved by using the :method:clusters/sparkVersions API call. |
| `spec.ssh_public_keys` | array<string> | SSH public key contents that will be added to each Spark node in this cluster. The corresponding private keys can be used to login with the user name `ubuntu` on port `2200`. Up to 10 keys can be specified. |
| `spec.use_ml_runtime` | boolean | This field can only be used when `kind = CLASSIC_PREVIEW`.  `effective_spark_version` is determined by `spark_version` (DBR release), this field `use_ml_runtime`, and whether `node_type_id` is gpu node or not. |
| `spec.worker_node_type_flexibility` | object | Configuration for flexible node types, allowing fallback to alternate node types during cluster launch and upscale. |
| `spec.worker_node_type_flexibility.alternate_node_type_ids` | array<string> | A list of node type IDs to use as fallbacks when the primary node type is unavailable. |
| `spec.workload_type` | object | Cluster Attributes showing for clusters workload types. |
| `spec.workload_type.clients` | object |  |
| `spec.workload_type.clients.jobs` | boolean | With jobs set, the cluster can be used for jobs |
| `spec.workload_type.clients.notebooks` | boolean | With notebooks set, this cluster can be used for notebooks |
| `ssh_public_keys` | array<string> | SSH public key contents that will be added to each Spark node in this cluster. The corresponding private keys can be used to login with the user name `ubuntu` on port `2200`. Up to 10 keys can be specified. |
| `start_time` | number | Time (in epoch milliseconds) when the cluster creation request was received (when the cluster entered a `PENDING` state). |
| `state` | string | The state of a Cluster. The current allowable state transitions are as follows:  - `PENDING` -> `RUNNING` - `PENDING` -> `TERMINATING` - `RUNNING` -> `RESIZING` - `RUNNING` -> `RESTARTING` - `RUNNING` -> `TERMINATING` - `RESTARTING` -> `RUNNING` - `RESTARTING` -> `TERMINATING` - `RESIZING` -> `RUNNING` - `RESIZING` -> `TERMINATING` - `TERMINATING` -> `TERMINATED` |
| `state_message` | string | A message associated with the most recent state transition (e.g., the reason why the cluster entered a `TERMINATED` state). |
| `terminated_time` | number | Time (in epoch milliseconds) when the cluster was terminated, if applicable. |
| `termination_reason` | object |  |
| `termination_reason.code` | string | The status code indicating why the cluster was terminated |
| `termination_reason.parameters` | object | list of parameters that provide additional information about why the cluster was terminated |
| `termination_reason.type` | string | type of the termination |
| `use_ml_runtime` | boolean | This field can only be used when `kind = CLASSIC_PREVIEW`.  `effective_spark_version` is determined by `spark_version` (DBR release), this field `use_ml_runtime`, and whether `node_type_id` is gpu node or not. |
| `worker_node_type_flexibility` | object | Configuration for flexible node types, allowing fallback to alternate node types during cluster launch and upscale. |
| `worker_node_type_flexibility.alternate_node_type_ids` | array<string> | A list of node type IDs to use as fallbacks when the primary node type is unavailable. |
| `workload_type` | object | Cluster Attributes showing for clusters workload types. |
| `workload_type.clients` | object |  |
| `workload_type.clients.jobs` | boolean | With jobs set, the cluster can be used for jobs |
| `workload_type.clients.notebooks` | boolean | With notebooks set, this cluster can be used for notebooks |

## Native endpoint

Through the native Databricks API, this operation is `GET {{credentials.host}}/api/2.1/clusters/list` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clusters.md) for the provider-specific parameters and requirements.

