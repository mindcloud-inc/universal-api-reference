# Databricks: Update Cluster

Updates an existing cluster in the Databricks workspace.

```
PUT https://connect.mindcloud.co/v1/universal/databricks/latest/actions/update-cluster
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/update-cluster" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clusterId": "string",
  "updateMask": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/databricks/latest/actions/update-cluster', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clusterId": "string",
    "updateMask": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cluster` | object | no |  |
| `cluster.autoscale` | object | no |  |
| `cluster.autoterminationMinutes` | number | no | Automatically terminates the cluster after it is inactive for this time in minutes. If not set, this cluster will not be automatically terminated. If specified, the threshold must be between 10 and 10000 minutes. Users can also set this value to 0 to explicitly disable automatic termination. |
| `cluster.awsAttributes` | object | no | Attributes set during cluster creation which are related to Amazon Web Services. |
| `cluster.clusterLogConf` | object | no | Cluster log delivery config |
| `cluster.clusterName` | string | no | Cluster name requested by the user. This doesn't have to be unique. If not specified at creation, the cluster name will be an empty string. For job clusters, the cluster name is automatically set based on the job and job run IDs. |
| `cluster.customTags` | object | no | Additional tags for cluster resources. Databricks will tag all cluster resources (e.g., AWS instances and EBS volumes) with these tags in addition to `default_tags`. Notes: - Currently, Databricks allows at most 45 custom tags - Clusters can only reuse cloud resources if the resources' tags are a subset of the cluster tags |
| `cluster.dataSecurityMode` | string | no | Data security mode decides what data governance model to use when accessing data from a cluster. The following modes can only be used when `kind = CLASSIC_PREVIEW`. * `DATA_SECURITY_MODE_AUTO`: Databricks will choose the most appropriate access mode depending on your compute configuration. * `DATA_SECURITY_MODE_STANDARD`: Alias for `USER_ISOLATION`. * `DATA_SECURITY_MODE_DEDICATED`: Alias for `SINGLE_USER`. The following modes can be used regardless of `kind`. * `NONE`: No security isolation for multiple users sharing the cluster. Data governance features are not available in this mode. * `SINGLE_USER`: A secure cluster that can only be exclusively used by a single user specified in `single_user_name`. Most programming languages, cluster features and data governance features are available in this mode. * `USER_ISOLATION`: A secure cluster that can be shared by multiple users. Cluster users are fully isolated so that they cannot see each other's data and credentials. Most data governance features are supported in this mode. But programming languages and cluster features might be limited. The following modes are deprecated starting with Databricks Runtime 15.0 and will be removed for future Databricks Runtime versions: * `LEGACY_TABLE_ACL`: This mode is for users migrating from legacy Table ACL clusters. * `LEGACY_PASSTHROUGH`: This mode is for users migrating from legacy Passthrough on high concurrency clusters. * `LEGACY_SINGLE_USER`: This mode is for users migrating from legacy Passthrough on standard clusters. * `LEGACY_SINGLE_USER_STANDARD`: This mode provides a way that doesnât have UC nor passthrough enabled. |
| `cluster.dockerImage` | object | no |  |
| `cluster.driverInstancePoolId` | string | no | The optional ID of the instance pool for the driver of the cluster belongs. The pool cluster uses the instance pool with id (instance_pool_id) if the driver pool is not assigned. |
| `cluster.driverNodeTypeFlexibility` | object | no | Configuration for flexible node types, allowing fallback to alternate node types during cluster launch and upscale. |
| `cluster.driverNodeTypeId` | string | no | The node type of the Spark driver. Note that this field is optional; if unset, the driver node type will be set as the same value as `node_type_id` defined above. This field, along with node_type_id, should not be set if virtual_cluster_size is set. If both driver_node_type_id, node_type_id, and virtual_cluster_size are specified, driver_node_type_id and node_type_id take precedence. |
| `cluster.enableElasticDisk` | boolean | no | Autoscaling Local Storage: when enabled, this cluster will dynamically acquire additional disk space when its Spark workers are running low on disk space. This feature requires specific AWS permissions to function correctly - refer to the User Guide for more details. |
| `cluster.enableLocalDiskEncryption` | boolean | no | Whether to enable LUKS on cluster VMs' local disks |
| `cluster.initScripts` | list<string> | no | The configuration for storing init scripts. Any number of destinations can be specified. The scripts are executed sequentially in the order provided. If `cluster_log_conf` is specified, init script logs are sent to `<destination>/<cluster-ID>/init_scripts`. |
| `cluster.instancePoolId` | string | no | The optional ID of the instance pool to which the cluster belongs. |
| `cluster.isSingleNode` | boolean | no | This field can only be used when `kind = CLASSIC_PREVIEW`. When set to true, Databricks will automatically set single node related `custom_tags`, `spark_conf`, and `num_workers` |
| `cluster.kind` | string | no | The kind of compute described by this compute specification. Depending on `kind`, different validations and default values will be applied. Clusters with `kind = CLASSIC_PREVIEW` support the following fields, whereas clusters with no specified `kind` do not. * [is_single_node](/api/workspace/clusters/create#is_single_node) * [use_ml_runtime](/api/workspace/clusters/create#use_ml_runtime) * [data_security_mode](/api/workspace/clusters/create#data_security_mode) set to `DATA_SECURITY_MODE_AUTO`, `DATA_SECURITY_MODE_DEDICATED`, or `DATA_SECURITY_MODE_STANDARD` By using the [simple form](https://docs.databricks.com/compute/simple-form.html), your clusters are automatically using `kind = CLASSIC_PREVIEW`. |
| `cluster.nodeTypeId` | string | no | This field encodes, through a single value, the resources available to each of the Spark nodes in this cluster. For example, the Spark nodes can be provisioned and optimized for memory or compute intensive workloads. A list of available node types can be retrieved by using the :method:clusters/listNodeTypes API call. |
| `cluster.numWorkers` | number | no | Number of worker nodes that this cluster should have. A cluster has one Spark Driver and `num_workers` Executors for a total of `num_workers` + 1 Spark nodes. Note: When reading the properties of a cluster, this field reflects the desired number of workers rather than the actual current number of workers. For instance, if a cluster is resized from 5 to 10 workers, this field will immediately be updated to reflect the target size of 10 workers, whereas the workers listed in `spark_info` will gradually increase from 5 to 10 as the new nodes are provisioned. |
| `cluster.policyId` | string | no | The ID of the cluster policy used to create the cluster if applicable. |
| `cluster.runtimeEngine` | string | no |  |
| `cluster.singleUserName` | string | no | Single user name if data_security_mode is `SINGLE_USER` |
| `cluster.sparkConf` | object | no | An object containing a set of optional, user-specified Spark configuration key-value pairs. Users can also pass in a string of extra JVM options to the driver and the executors via `spark.driver.extraJavaOptions` and `spark.executor.extraJavaOptions` respectively. |
| `cluster.sparkEnvVars` | object | no | An object containing a set of optional, user-specified environment variable key-value pairs. Please note that key-value pair of the form (X,Y) will be exported as is (i.e., `export X='Y'`) while launching the driver and workers. In order to specify an additional set of `SPARK_DAEMON_JAVA_OPTS`, we recommend appending them to `$SPARK_DAEMON_JAVA_OPTS` as shown in the example below. This ensures that all default databricks managed environmental variables are included as well. Example Spark environment variables: `{"SPARK_WORKER_MEMORY": "28000m", "SPARK_LOCAL_DIRS": "/local_disk0"}` or `{"SPARK_DAEMON_JAVA_OPTS": "$SPARK_DAEMON_JAVA_OPTS -Dspark.shuffle.service.enabled=true"}` |
| `cluster.sparkVersion` | string | no | The Spark version of the cluster, e.g. `3.3.x-scala2.11`. A list of available Spark versions can be retrieved by using the :method:clusters/sparkVersions API call. |
| `cluster.sshPublicKeys` | list<string> | no | SSH public key contents that will be added to each Spark node in this cluster. The corresponding private keys can be used to login with the user name `ubuntu` on port `2200`. Up to 10 keys can be specified. |
| `cluster.useMlRuntime` | boolean | no | This field can only be used when `kind = CLASSIC_PREVIEW`. `effective_spark_version` is determined by `spark_version` (DBR release), this field `use_ml_runtime`, and whether `node_type_id` is gpu node or not. |
| `cluster.workerNodeTypeFlexibility` | object | no | Configuration for flexible node types, allowing fallback to alternate node types during cluster launch and upscale. |
| `cluster.workloadType` | object | no | Cluster Attributes showing for clusters workload types. |
| `clusterId` | string | yes | ID of the cluster. |
| `updateMask` | string | yes | Used to specify which cluster attributes and size fields to update. See https://google.aip.dev/161 for more details. The field mask must be a single string, with multiple fields separated by commas (no spaces). The field path is relative to the resource object, using a dot (`.`) to navigate sub-fields (e.g., `author.given_name`). Specification of elements in sequence or map fields is not allowed, as only the entire collection field can be specified. Field names must exactly match the resource field names. A field mask of `*` indicates full replacement. Itâs recommended to always explicitly list the fields being updated and avoid using `*` wildcards, as it can lead to unintended results if the API changes in the future. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cluster_id": "string",
      "cluster_name": "Ava Chen",
      "state": "string",
      "state_message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cluster_id` | string | Canonical identifier for the cluster. |
| `cluster_name` | string | Cluster name. |
| `state` | string | Current cluster state. |
| `state_message` | string | State transition message. |

## Native endpoint

Through the native Databricks API, this operation is `POST {{credentials.host}}/api/2.1/clusters/update` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-cluster.md) for the provider-specific parameters and requirements.

