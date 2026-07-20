# Neon: Delete JWKS URL

Deletes a JWKS URL from a project in Neon.

```
DELETE https://connect.mindcloud.co/v1/universal/neon/latest/actions/delete-project-jwks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/neon/latest/actions/delete-project-jwks?connectionId=$CONNECTION_ID&project_id=string&jwks_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string",
  "jwks_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/delete-project-jwks?${params}`, {
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
| `jwks_id` | string | yes | Neon API parameter jwks_id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branch_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "jwks_url": "https://example.com",
      "jwt_audience": "string",
      "project_id": "string",
      "provider_name": "Ava Chen",
      "role_names": [
        "Ava Chen"
      ],
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branch_id` | string |  |
| `created_at` | date |  |
| `id` | string |  |
| `jwks_url` | string |  |
| `jwt_audience` | string |  |
| `project_id` | string |  |
| `provider_name` | string |  |
| `role_names` | array<string> |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Neon API, this operation is `DELETE /projects/:project_id/jwks/:jwks_id` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project-jwks.md) for the provider-specific parameters and requirements.

