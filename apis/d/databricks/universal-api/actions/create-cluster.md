# Databricks: Create Cluster

Creates a new cluster in the Databricks workspace.

```
POST https://connect.mindcloud.co/v1/universal/databricks/latest/actions/create-cluster
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/create-cluster" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cloneFrom.sourceClusterId": "string",
  "initScripts": "string",
  "sparkVersion": "string",
  "sshPublicKeys": "string",
  "workloadType.clients": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/databricks/latest/actions/create-cluster', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cloneFrom.sourceClusterId": "string",
    "initScripts": "string",
    "sparkVersion": "string",
    "sshPublicKeys": "string",
    "workloadType.clients": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `applyPolicyDefaultValues` | boolean | no | When set to true, fixed and default values from the policy will be used for fields that are omitted. When set to false, only fixed values from the policy will be applied. |
| `autoscale` | object | no |  |
| `autoscale.maxWorkers` | number | no | The maximum number of workers to which the cluster can scale up when overloaded. Note that `max_workers` must be strictly greater than `min_workers`. |
| `autoscale.minWorkers` | number | no | The minimum number of workers to which the cluster can scale down when underutilized. It is also the initial number of workers the cluster will have after creation. |
| `autoterminationMinutes` | number | no | Automatically terminates the cluster after it is inactive for this time in minutes. If not set, this cluster will not be automatically terminated. If specified, the threshold must be between 10 and 10000 minutes. Users can also set this value to 0 to explicitly disable automatic termination. |
| `awsAttributes` | object | no | Attributes set during cluster creation which are related to Amazon Web Services. |
| `awsAttributes.availability` | string | no | Availability type used for all subsequent nodes past the `first_on_demand` ones. Note: If `first_on_demand` is zero, this availability type will be used for the entire cluster. |
| `awsAttributes.ebsVolumeCount` | number | no | The number of volumes launched for each instance. Users can choose up to 10 volumes. This feature is only enabled for supported node types. Legacy node types cannot specify custom EBS volumes. For node types with no instance store, at least one EBS volume needs to be specified; otherwise, cluster creation will fail. These EBS volumes will be mounted at `/ebs0`, `/ebs1`, and etc. Instance store volumes will be mounted at `/local_disk0`, `/local_disk1`, and etc. If EBS volumes are attached, Databricks will configure Spark to use only the EBS volumes for scratch storage because heterogenously sized scratch devices can lead to inefficient disk utilization. If no EBS volumes are attached, Databricks will configure Spark to use instance store volumes. Please note that if EBS volumes are specified, then the Spark configuration `spark.local.dir` will be overridden. |
| `awsAttributes.ebsVolumeIops` | number | no | If using gp3 volumes, what IOPS to use for the disk. If this is not set, the maximum performance of a gp2 volume with the same volume size will be used. |
| `awsAttributes.ebsVolumeSize` | number | no | The size of each EBS volume (in GiB) launched for each instance. For general purpose SSD, this value must be within the range 100 - 4096. For throughput optimized HDD, this value must be within the range 500 - 4096. |
| `awsAttributes.ebsVolumeThroughput` | number | no | If using gp3 volumes, what throughput to use for the disk. If this is not set, the maximum performance of a gp2 volume with the same volume size will be used. |
| `awsAttributes.ebsVolumeType` | string | no | All EBS volume types that Databricks supports. See https://aws.amazon.com/ebs/details/ for details. |
| `awsAttributes.firstOnDemand` | number | no | The first `first_on_demand` nodes of the cluster will be placed on on-demand instances. If this value is greater than 0, the cluster driver node in particular will be placed on an on-demand instance. If this value is greater than or equal to the current cluster size, all nodes will be placed on on-demand instances. If this value is less than the current cluster size, `first_on_demand` nodes will be placed on on-demand instances and the remainder will be placed on `availability` instances. Note that this value does not affect cluster size and cannot currently be mutated over the lifetime of a cluster. |
| `awsAttributes.instanceProfileArn` | string | no | Nodes for this cluster will only be placed on AWS instances with this instance profile. If ommitted, nodes will be placed on instances without an IAM instance profile. The instance profile must have previously been added to the Databricks environment by an account administrator. This feature may only be available to certain customer plans. |
| `awsAttributes.spotBidPricePercent` | number | no | The bid price for AWS spot instances, as a percentage of the corresponding instance type's on-demand price. For example, if this field is set to 50, and the cluster needs a new `r3.xlarge` spot instance, then the bid price is half of the price of on-demand `r3.xlarge` instances. Similarly, if this field is set to 200, the bid price is twice the price of on-demand `r3.xlarge` instances. If not specified, the default value is 100. When spot instances are requested for this cluster, only spot instances whose bid price percentage matches this field will be considered. Note that, for safety, we enforce this field to be no more than 10000. |
| `awsAttributes.zoneId` | string | no | Identifier for the availability zone/datacenter in which the cluster resides. This string will be of a form like "us-west-2a". The provided availability zone must be in the same region as the Databricks deployment. For example, "us-west-2a" is not a valid zone id if the Databricks deployment resides in the "us-east-1" region. This is an optional field at cluster creation, and if not specified, the zone "auto" will be used. If the zone specified is "auto", will try to place cluster in a zone with high availability, and will retry placement in a different AZ if there is not enough capacity. The list of available zones as well as the default value can be found by using the `List Zones` method. |
| `cloneFrom` | object | no |  |
| `cloneFrom.sourceClusterId` | string | yes | The cluster that is being cloned. |
| `clusterLogConf` | object | no | Cluster log delivery config |
| `clusterLogConf.dbfs` | object | no | A storage location in DBFS |
| `clusterLogConf.s3` | object | no | A storage location in Amazon S3 |
| `clusterLogConf.volumes` | object | no | A storage location back by UC Volumes. |
| `clusterName` | string | no | Cluster name requested by the user. This doesn't have to be unique. If not specified at creation, the cluster name will be an empty string. For job clusters, the cluster name is automatically set based on the job and job run IDs. |
| `customTags` | object | no | Additional tags for cluster resources. Databricks will tag all cluster resources (e.g., AWS instances and EBS volumes) with these tags in addition to `default_tags`. Notes: - Currently, Databricks allows at most 45 custom tags - Clusters can only reuse cloud resources if the resources' tags are a subset of the cluster tags |
| `dataSecurityMode` | string | no | Data security mode decides what data governance model to use when accessing data from a cluster. The following modes can only be used when `kind = CLASSIC_PREVIEW`. * `DATA_SECURITY_MODE_AUTO`: Databricks will choose the most appropriate access mode depending on your compute configuration. * `DATA_SECURITY_MODE_STANDARD`: Alias for `USER_ISOLATION`. * `DATA_SECURITY_MODE_DEDICATED`: Alias for `SINGLE_USER`. The following modes can be used regardless of `kind`. * `NONE`: No security isolation for multiple users sharing the cluster. Data governance features are not available in this mode. * `SINGLE_USER`: A secure cluster that can only be exclusively used by a single user specified in `single_user_name`. Most programming languages, cluster features and data governance features are available in this mode. * `USER_ISOLATION`: A secure cluster that can be shared by multiple users. Cluster users are fully isolated so that they cannot see each other's data and credentials. Most data governance features are supported in this mode. But programming languages and cluster features might be limited. The following modes are deprecated starting with Databricks Runtime 15.0 and will be removed for future Databricks Runtime versions: * `LEGACY_TABLE_ACL`: This mode is for users migrating from legacy Table ACL clusters. * `LEGACY_PASSTHROUGH`: This mode is for users migrating from legacy Passthrough on high concurrency clusters. * `LEGACY_SINGLE_USER`: This mode is for users migrating from legacy Passthrough on standard clusters. * `LEGACY_SINGLE_USER_STANDARD`: This mode provides a way that doesnât have UC nor passthrough enabled. |
| `dockerImage` | object | no |  |
| `dockerImage.basicAuth` | object | no |  |
| `dockerImage.url` | string | no | URL of the docker image. |
| `driverInstancePoolId` | string | no | The optional ID of the instance pool for the driver of the cluster belongs. The pool cluster uses the instance pool with id (instance_pool_id) if the driver pool is not assigned. |
| `driverNodeTypeFlexibility` | object | no | Configuration for flexible node types, allowing fallback to alternate node types during cluster launch and upscale. |
| `driverNodeTypeFlexibility.alternateNodeTypeIds` | list<string> | no | A list of node type IDs to use as fallbacks when the primary node type is unavailable. |
| `driverNodeTypeId` | string | no | The node type of the Spark driver. Note that this field is optional; if unset, the driver node type will be set as the same value as `node_type_id` defined above. This field, along with node_type_id, should not be set if virtual_cluster_size is set. If both driver_node_type_id, node_type_id, and virtual_cluster_size are specified, driver_node_type_id and node_type_id take precedence. |
| `enableElasticDisk` | boolean | no | Autoscaling Local Storage: when enabled, this cluster will dynamically acquire additional disk space when its Spark workers are running low on disk space. This feature requires specific AWS permissions to function correctly - refer to the User Guide for more details. |
| `enableLocalDiskEncryption` | boolean | no | Whether to enable LUKS on cluster VMs' local disks |
| `initScripts` | list<string> | yes | The configuration for storing init scripts. Any number of destinations can be specified. The scripts are executed sequentially in the order provided. If `cluster_log_conf` is specified, init script logs are sent to `<destination>/<cluster-ID>/init_scripts`. |
| `instancePoolId` | string | no | The optional ID of the instance pool to which the cluster belongs. |
| `isSingleNode` | boolean | no | This field can only be used when `kind = CLASSIC_PREVIEW`. When set to true, Databricks will automatically set single node related `custom_tags`, `spark_conf`, and `num_workers` |
| `kind` | string | no | The kind of compute described by this compute specification. Depending on `kind`, different validations and default values will be applied. Clusters with `kind = CLASSIC_PREVIEW` support the following fields, whereas clusters with no specified `kind` do not. * [is_single_node](/api/workspace/clusters/create#is_single_node) * [use_ml_runtime](/api/workspace/clusters/create#use_ml_runtime) * [data_security_mode](/api/workspace/clusters/create#data_security_mode) set to `DATA_SECURITY_MODE_AUTO`, `DATA_SECURITY_MODE_DEDICATED`, or `DATA_SECURITY_MODE_STANDARD` By using the [simple form](https://docs.databricks.com/compute/simple-form.html), your clusters are automatically using `kind = CLASSIC_PREVIEW`. |
| `nodeTypeId` | string | no | This field encodes, through a single value, the resources available to each of the Spark nodes in this cluster. For example, the Spark nodes can be provisioned and optimized for memory or compute intensive workloads. A list of available node types can be retrieved by using the :method:clusters/listNodeTypes API call. |
| `numWorkers` | number | no | Number of worker nodes that this cluster should have. A cluster has one Spark Driver and `num_workers` Executors for a total of `num_workers` + 1 Spark nodes. Note: When reading the properties of a cluster, this field reflects the desired number of workers rather than the actual current number of workers. For instance, if a cluster is resized from 5 to 10 workers, this field will immediately be updated to reflect the target size of 10 workers, whereas the workers listed in `spark_info` will gradually increase from 5 to 10 as the new nodes are provisioned. |
| `policyId` | string | no | The ID of the cluster policy used to create the cluster if applicable. |
| `runtimeEngine` | string | no |  |
| `singleUserName` | string | no | Single user name if data_security_mode is `SINGLE_USER` |
| `sparkConf` | object | no | An object containing a set of optional, user-specified Spark configuration key-value pairs. Users can also pass in a string of extra JVM options to the driver and the executors via `spark.driver.extraJavaOptions` and `spark.executor.extraJavaOptions` respectively. |
| `sparkEnvVars` | object | no | An object containing a set of optional, user-specified environment variable key-value pairs. Please note that key-value pair of the form (X,Y) will be exported as is (i.e., `export X='Y'`) while launching the driver and workers. In order to specify an additional set of `SPARK_DAEMON_JAVA_OPTS`, we recommend appending them to `$SPARK_DAEMON_JAVA_OPTS` as shown in the example below. This ensures that all default databricks managed environmental variables are included as well. Example Spark environment variables: `{"SPARK_WORKER_MEMORY": "28000m", "SPARK_LOCAL_DIRS": "/local_disk0"}` or `{"SPARK_DAEMON_JAVA_OPTS": "$SPARK_DAEMON_JAVA_OPTS -Dspark.shuffle.service.enabled=true"}` |
| `sparkVersion` | string | yes | The Spark version of the cluster, e.g. `3.3.x-scala2.11`. A list of available Spark versions can be retrieved by using the :method:clusters/sparkVersions API call. |
| `sshPublicKeys` | list<string> | yes | SSH public key contents that will be added to each Spark node in this cluster. The corresponding private keys can be used to login with the user name `ubuntu` on port `2200`. Up to 10 keys can be specified. |
| `useMlRuntime` | boolean | no | This field can only be used when `kind = CLASSIC_PREVIEW`. `effective_spark_version` is determined by `spark_version` (DBR release), this field `use_ml_runtime`, and whether `node_type_id` is gpu node or not. |
| `workerNodeTypeFlexibility` | object | no | Configuration for flexible node types, allowing fallback to alternate node types during cluster launch and upscale. |
| `workerNodeTypeFlexibility.alternateNodeTypeIds` | list<string> | no | A list of node type IDs to use as fallbacks when the primary node type is unavailable. |
| `workloadType` | object | no | Cluster Attributes showing for clusters workload types. |
| `workloadType.clients` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cluster_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cluster_id` | string |  |

## Native endpoint

Through the native Databricks API, this operation is `POST {{credentials.host}}/api/2.1/clusters/create` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-cluster.md) for the provider-specific parameters and requirements.

