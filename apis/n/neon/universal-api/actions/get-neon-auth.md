# Neon: Get details of Neon Auth for the branch

Retrieves Neon Auth details for the branch from Neon.

```
GET https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-neon-auth
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-neon-auth?connectionId=$CONNECTION_ID&project_id=string&branch_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string",
  "branch_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-neon-auth?${params}`, {
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
      "branch_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "db_name": "Ava Chen",
      "jwks_url": "https://example.com",
      "name": "Ava Chen",
      "owned_by": [
        "string"
      ],
      "transfer_status": [
        "string"
      ]
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
| `branch_id` | string |  |
| `created_at` | date |  |
| `db_name` | string |  |
| `jwks_url` | string |  |
| `name` | string |  |
| `owned_by` | array |  |
| `transfer_status` | array |  |

## Native endpoint

Through the native Neon API, this operation is `GET /projects/:project_id/branches/:branch_id/auth` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-neon-auth.md) for the provider-specific parameters and requirements.

