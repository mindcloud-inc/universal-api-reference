# Update Workspace with Databricks

Updates an existing workspace in the Databricks account.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/2.0/accounts/{accountId}/workspaces/:workspaceId`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Update Workspace](https://docs.databricks.com/api/account/workspaces/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | body | `number` | yes | A unique integer ID for the workspace |
| `account_id` | body | `string` | no | Databricks account ID. |
| `aws_region` | body | `string` | no | The AWS region of the workspace data plane (for example, `us-west-2`). |
| `compute_mode` | body | `string` | no | Corresponds to compute mode defined here: https://src.dev.databricks.com/databricks/universe@9076536b18479afd639d1c1f9dd5a59f72215e69/-/blob/central/api/common.proto?L872 |
| `creation_time` | body | `number` | no | Time in epoch milliseconds when the workspace was created. |
| `credentials_id` | body | `string` | no | ID of the workspace's credential configuration object. |
| `custom_tags` | body | `object` | no | The custom tags key-value pairing that is attached to this workspace. The key-value pair is a string of utf-8 characters. The value can be an empty string, with maximum length of 255 characters. The key can be of maximum length of 127 characters, and cannot be empty. |
| `deployment_name` | body | `string` | no | The deployment name defines part of the subdomain for the workspace. The workspace URL for web application and REST APIs is `<deployment-name>.cloud.databricks.com`. |
| `managed_services_customer_managed_key_id` | body | `string` | no | ID of the key configuration for encrypting managed services. |
| `network_connectivity_config_id` | body | `string` | no | The object ID of network connectivity config. |
| `network_id` | body | `string` | no | If this workspace is BYO VPC, then the network_id will be populated. If this workspace is not BYO VPC, then the network_id will be empty. |
| `pricing_tier` | body | `string` | no | — |
| `private_access_settings_id` | body | `string` | no | ID of the workspace's private access settings object. Only used for PrivateLink. You must specify this ID if you are using [AWS PrivateLink](https://aws.amazon.com/privatelink/) for either front-end (user-to-workspace connection), back-end (data plane to control plane connection), or both connection types.  Before configuring PrivateLink, read the [Databricks article about PrivateLink](https://docs.databricks.com/administration-guide/cloud-configurations/aws/privatelink.html).", |
| `storage_configuration_id` | body | `string` | no | ID of the workspace's storage configuration object. |
| `storage_customer_managed_key_id` | body | `string` | no | ID of the key configuration for encrypting workspace storage. |
| `storage_mode` | body | `string` | no | — |
| `workspace_name` | body | `string` | no | The human-readable name of the workspace. |
| `workspace_status` | body | `string` | no | The different statuses of a workspace. The following represents the current set of valid transitions from status to status: NOT_PROVISIONED -> PROVISIONING -> CANCELLED PROVISIONING -> RUNNING -> FAILED -> CANCELLED (note that this transition is disallowed in the MultiWorkspace Project) RUNNING -> PROVISIONING -> BANNED -> CANCELLED FAILED -> PROVISIONING -> CANCELLED BANNED -> RUNNING -> CANCELLED Note that a transition from any state to itself is also valid. TODO(PLAT-5867): add a transition from CANCELLED to some other value (e.g. RECOVERING) |
| `workspace_status_message` | body | `string` | no | Message describing the current workspace status. |
