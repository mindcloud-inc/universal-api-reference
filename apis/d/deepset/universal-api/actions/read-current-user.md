# Deepset: Read Current User

Retrieves the current user from Deepset.

```
GET https://connect.mindcloud.co/v1/universal/deepset/latest/actions/read-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepset/latest/actions/read-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepset/latest/actions/read-current-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "email": "ava@example.com",
      "family_name": "Ava Chen",
      "given_name": "Ava Chen",
      "oauth_id": "string",
      "oauth_provider": "string",
      "organization": {
        "gpu_enabled": true,
        "local_builder_enabled": true,
        "max_workspaces": 1,
        "name": "Ava Chen",
        "organization_id": "string",
        "organization_type": "string",
        "role": "string",
        "workspaces": [
          {
            "name": "Ava Chen",
            "role": "string",
            "role_id": "string"
          }
        ]
      },
      "user_id": "string",
      "userflow_signature": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `email` | string |  |
| `family_name` | string |  |
| `given_name` | string |  |
| `oauth_id` | string |  |
| `oauth_provider` | string |  |
| `organization.gpu_enabled` | boolean |  |
| `organization.local_builder_enabled` | boolean |  |
| `organization.max_workspaces` | number |  |
| `organization.name` | string |  |
| `organization.organization_id` | string |  |
| `organization.organization_type` | string |  |
| `organization.role` | string |  |
| `organization.workspaces[].name` | string |  |
| `organization.workspaces[].role` | string |  |
| `organization.workspaces[].role_id` | string |  |
| `user_id` | string |  |
| `userflow_signature` | string |  |

## Native endpoint

Through the native Deepset API, this operation is `GET /api/v1/me` (base URL `https://api.cloud.deepset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-current-user.md) for the provider-specific parameters and requirements.

