# Neon: Retrieve role password

Retrieves a role password from Neon.

```
GET https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-project-branch-role-password
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-project-branch-role-password?connectionId=$CONNECTION_ID&project_id=string&branch_id=string&role_name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string",
  "branch_id": "string",
  "role_name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-project-branch-role-password?${params}`, {
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
| `project_id` | string | yes | Neon API parameter project_id |
| `branch_id` | string | yes | Neon API parameter branch_id |
| `role_name` | string | yes | Neon API parameter role_name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "password": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `password` | string |  |

## Native endpoint

Through the native Neon API, this operation is `GET /projects/:project_id/branches/:branch_id/roles/:role_name/reveal_password` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-branch-role-password.md) for the provider-specific parameters and requirements.

