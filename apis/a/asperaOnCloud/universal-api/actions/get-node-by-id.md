# Aspera on Cloud: Get Node

Retrieves a node from Aspera on Cloud.

```
GET https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/get-node-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspera on Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/get-node-by-id?connectionId=$CONNECTION_ID&id=node_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "node_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/get-node-by-id?${params}`, {
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
| `id` | string | yes | ID of the node. Example: `node_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_key": "string",
      "ats_access_key": true,
      "ats_storage_type": "string",
      "capabilities": {
        "name": "Ava Chen",
        "value": "string"
      },
      "configuration_policy_id": 1,
      "error_message": "string",
      "error_time": "string",
      "host": "string",
      "name": "Ava Chen",
      "network_policy_id": 1,
      "path": "string",
      "port": 1,
      "settings": {
        "name": "Ava Chen",
        "value": "string"
      },
      "ssh_fingerprint": "string",
      "status": "string",
      "url": "https://example.com",
      "use_ssl": true,
      "verify_ssl_certificate": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_key` | string |  |
| `ats_access_key` | boolean |  |
| `ats_storage_type` | string |  |
| `capabilities.name` | string |  |
| `capabilities.value` | string |  |
| `configuration_policy_id` | number |  |
| `error_message` | string |  |
| `error_time` | string |  |
| `host` | string |  |
| `name` | string |  |
| `network_policy_id` | number |  |
| `path` | string |  |
| `port` | number |  |
| `settings.name` | string |  |
| `settings.value` | string |  |
| `ssh_fingerprint` | string |  |
| `status` | string |  |
| `url` | string |  |
| `use_ssl` | boolean |  |
| `verify_ssl_certificate` | boolean |  |

## Native endpoint

Through the native Aspera on Cloud API, this operation is `GET /v1/nodes/{id}` (base URL `https://api.ibmaspera.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-node-by-id.md) for the provider-specific parameters and requirements.

