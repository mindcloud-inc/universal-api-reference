# Databricks: Get Workspace

Retrieves a workspace from the Databricks account.

```
GET https://connect.mindcloud.co/v1/universal/databricks/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/get-workspace?connectionId=$CONNECTION_ID&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/databricks/latest/actions/get-workspace?${params}`, {
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
| `workspaceId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": "string",
      "aws_region": "string",
      "compute_mode": "string",
      "creation_time": 1,
      "credentials_id": "string",
      "custom_tags": {},
      "deployment_name": "Ava Chen",
      "managed_services_customer_managed_key_id": "string",
      "network_connectivity_config_id": "string",
      "network_id": "string",
      "pricing_tier": "string",
      "private_access_settings_id": "string",
      "storage_configuration_id": "string",
      "storage_customer_managed_key_id": "string",
      "storage_mode": "string",
      "workspace_id": 1,
      "workspace_name": "Ava Chen",
      "workspace_status": "string",
      "workspace_status_message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | string | Databricks account ID. |
| `aws_region` | string | The AWS region of the workspace data plane (for example, `us-west-2`). |
| `compute_mode` | string | Corresponds to compute mode defined here: https://src.dev.databricks.com/databricks/universe@9076536b18479afd639d1c1f9dd5a59f72215e69/-/blob/central/api/common.proto?L872 |
| `creation_time` | number | Time in epoch milliseconds when the workspace was created. |
| `credentials_id` | string | ID of the workspace's credential configuration object. |
| `custom_tags` | object | The custom tags key-value pairing that is attached to this workspace. The key-value pair is a string of utf-8 characters. The value can be an empty string, with maximum length of 255 characters. The key can be of maximum length of 127 characters, and cannot be empty. |
| `deployment_name` | string | The deployment name defines part of the subdomain for the workspace. The workspace URL for web application and REST APIs is `<deployment-name>.cloud.databricks.com`. |
| `managed_services_customer_managed_key_id` | string | ID of the key configuration for encrypting managed services. |
| `network_connectivity_config_id` | string | The object ID of network connectivity config. |
| `network_id` | string | If this workspace is BYO VPC, then the network_id will be populated. If this workspace is not BYO VPC, then the network_id will be empty. |
| `pricing_tier` | string |  |
| `private_access_settings_id` | string | ID of the workspace's private access settings object. Only used for PrivateLink. You must specify this ID if you are using [AWS PrivateLink](https://aws.amazon.com/privatelink/) for either front-end (user-to-workspace connection), back-end (data plane to control plane connection), or both connection types.  Before configuring PrivateLink, read the [Databricks article about PrivateLink](https://docs.databricks.com/administration-guide/cloud-configurations/aws/privatelink.html).", |
| `storage_configuration_id` | string | ID of the workspace's storage configuration object. |
| `storage_customer_managed_key_id` | string | ID of the key configuration for encrypting workspace storage. |
| `storage_mode` | string |  |
| `workspace_id` | number | A unique integer ID for the workspace |
| `workspace_name` | string | The human-readable name of the workspace. |
| `workspace_status` | string | The different statuses of a workspace. The following represents the current set of valid transitions from status to status: NOT_PROVISIONED -> PROVISIONING -> CANCELLED PROVISIONING -> RUNNING -> FAILED -> CANCELLED (note that this transition is disallowed in the MultiWorkspace Project) RUNNING -> PROVISIONING -> BANNED -> CANCELLED FAILED -> PROVISIONING -> CANCELLED BANNED -> RUNNING -> CANCELLED Note that a transition from any state to itself is also valid. TODO(PLAT-5867): add a transition from CANCELLED to some other value (e.g. RECOVERING) |
| `workspace_status_message` | string | Message describing the current workspace status. |

## Native endpoint

Through the native Databricks API, this operation is `GET /api/2.0/accounts/{{credentials.accountId}}/workspaces/:workspaceId` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.

