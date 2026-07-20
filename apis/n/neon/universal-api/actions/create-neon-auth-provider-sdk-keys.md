# Neon: Create Auth Provider SDK keys

Creates auth provider SDK keys in Neon.

```
POST https://connect.mindcloud.co/v1/universal/neon/latest/actions/create-neon-auth-provider-sdk-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neon/latest/actions/create-neon-auth-provider-sdk-keys" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string",
  "auth_provider": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/create-neon-auth-provider-sdk-keys', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "string",
    "auth_provider": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | string | yes | Neon API parameter project_id |
| `auth_provider` | list | yes | Neon API parameter auth_provider One of: `0`, `1`, `2`, `3`. |

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

Through the native Neon API, this operation is `POST /projects/auth/keys` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-neon-auth-provider-sdk-keys.md) for the provider-specific parameters and requirements.

