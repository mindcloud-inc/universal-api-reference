# Aspera on Cloud: Create User

Creates a new user in Aspera on Cloud.

```
POST https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/add-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspera on Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/add-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/add-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "ats_admin": true,
      "available_apps": "string",
      "created_at": "string",
      "deactivated": true,
      "default_shortlink_name": "https://example.com",
      "default_workspace_choice": "string",
      "default_workspace_id": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "home_file_id": 1,
      "home_node_id": 1,
      "id": 1,
      "last_login_at": "string",
      "last_login_provider": "string",
      "last_name": "Chen",
      "member_of_any_workspace": true,
      "name": "Ava Chen",
      "organization_admin": true,
      "organization_id": 1,
      "password_updated_at": "string",
      "provisioned": true,
      "public_key": true,
      "read_only_home_file_id": "string",
      "read_only_home_node_id": 1,
      "running_operation_count": 1,
      "saml_configuration_id": "string",
      "stopped_operation_count": 1,
      "subscription_admin": true,
      "trial": true,
      "updated_at": "string",
      "user_admin": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ats_admin` | boolean |  |
| `available_apps` | string |  |
| `created_at` | string |  |
| `deactivated` | boolean |  |
| `default_shortlink_name` | string |  |
| `default_workspace_choice` | string |  |
| `default_workspace_id` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `home_file_id` | number |  |
| `home_node_id` | number |  |
| `id` | number |  |
| `last_login_at` | string |  |
| `last_login_provider` | string |  |
| `last_name` | string |  |
| `member_of_any_workspace` | boolean |  |
| `name` | string |  |
| `organization_admin` | boolean |  |
| `organization_id` | number |  |
| `password_updated_at` | string |  |
| `provisioned` | boolean |  |
| `public_key` | boolean |  |
| `read_only_home_file_id` | string |  |
| `read_only_home_node_id` | number |  |
| `running_operation_count` | number |  |
| `saml_configuration_id` | string |  |
| `stopped_operation_count` | number |  |
| `subscription_admin` | boolean |  |
| `trial` | boolean |  |
| `updated_at` | string |  |
| `user_admin` | boolean |  |

## Native endpoint

Through the native Aspera on Cloud API, this operation is `POST /v1/users` (base URL `https://api.ibmaspera.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-user.md) for the provider-specific parameters and requirements.

