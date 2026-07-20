# Neon: Create Neon Auth integration

Creates Neon Auth integration in Neon.

```
POST https://connect.mindcloud.co/v1/universal/neon/latest/actions/create-neon-auth-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neon/latest/actions/create-neon-auth-integration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "auth_provider": "0",
  "project_id": "string",
  "branch_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/create-neon-auth-integration', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "auth_provider": "0",
    "project_id": "string",
    "branch_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `auth_provider` | list | yes | Neon API parameter auth_provider One of: `0`, `1`, `2`, `3`. |
| `project_id` | string | yes | Neon API parameter project_id |
| `branch_id` | string | yes | Neon API parameter branch_id |
| `database_name` | string | no | Neon API parameter database_name |
| `role_name` | string | no | Neon API parameter role_name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auth_provider": [
        "string"
      ],
      "auth_provider_project_id": "string",
      "base_url": "https://example.com",
      "jwks_url": "https://example.com",
      "pub_client_key": "string",
      "schema_name": "Ava Chen",
      "secret_server_key": "string",
      "table_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auth_provider` | array |  |
| `auth_provider_project_id` | string |  |
| `base_url` | string |  |
| `jwks_url` | string |  |
| `pub_client_key` | string |  |
| `schema_name` | string |  |
| `secret_server_key` | string |  |
| `table_name` | string |  |

## Native endpoint

Through the native Neon API, this operation is `POST /projects/auth/create` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-neon-auth-integration.md) for the provider-specific parameters and requirements.

