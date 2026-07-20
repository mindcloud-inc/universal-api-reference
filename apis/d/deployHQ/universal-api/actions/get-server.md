# DeployHQ: Get Server

Retrieves a server from DeployHQ.

```
GET https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/get-server
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeployHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/get-server?connectionId=$CONNECTION_ID&projectId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/get-server?${params}`, {
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
| `projectId` | string | yes | The identifier or permalink of the project. |
| `id` | string | yes | The identifier of the server. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent": "string",
      "atomic": true,
      "atomic_retention": 1,
      "atomic_strategy": "string",
      "auto_deploy": true,
      "branch": "string",
      "connection_checked_at": "2026-05-07T12:00:00.000Z",
      "connection_error_message": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "environment": "string",
      "host_key": "string",
      "hostname": "Ava Chen",
      "id": 1,
      "identifier": "string",
      "last_revision": "string",
      "name": "Ava Chen",
      "notify_email": "ava@example.com",
      "port": "string",
      "position": 1,
      "preferred_branch": "string",
      "protocol_type": "string",
      "root_path": "string",
      "server_group_identifier": "string",
      "server_path": "string",
      "unlink_before_upload": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "use_accelerated_transfer": true,
      "use_compression": true,
      "use_parallel_upload": true,
      "use_ssh_keys": true,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent` | string |  |
| `atomic` | boolean |  |
| `atomic_retention` | number |  |
| `atomic_strategy` | string |  |
| `auto_deploy` | boolean |  |
| `branch` | string |  |
| `connection_checked_at` | date |  |
| `connection_error_message` | string |  |
| `created_at` | date |  |
| `enabled` | boolean |  |
| `environment` | string |  |
| `host_key` | string |  |
| `hostname` | string |  |
| `id` | number |  |
| `identifier` | string |  |
| `last_revision` | string |  |
| `name` | string |  |
| `notify_email` | string |  |
| `port` | string |  |
| `position` | number |  |
| `preferred_branch` | string |  |
| `protocol_type` | string |  |
| `root_path` | string |  |
| `server_group_identifier` | string |  |
| `server_path` | string |  |
| `unlink_before_upload` | boolean |  |
| `updated_at` | date |  |
| `use_accelerated_transfer` | boolean |  |
| `use_compression` | boolean |  |
| `use_parallel_upload` | boolean |  |
| `use_ssh_keys` | boolean |  |
| `username` | string |  |

## Native endpoint

Through the native DeployHQ API, this operation is `GET /projects/:project_id/servers/:id` (base URL `https://{{credentials.account}}.deployhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-server.md) for the provider-specific parameters and requirements.

