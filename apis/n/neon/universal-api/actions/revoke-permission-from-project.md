# Neon: Revoke project access

Revokes a project access from Neon.

```
DELETE https://connect.mindcloud.co/v1/universal/neon/latest/actions/revoke-permission-from-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/neon/latest/actions/revoke-permission-from-project?connectionId=$CONNECTION_ID&project_id=string&permission_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string",
  "permission_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/revoke-permission-from-project?${params}`, {
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
| `permission_id` | string | yes | Neon API parameter permission_id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "granted_at": "2026-05-07T12:00:00.000Z",
      "granted_to_email": "ava@example.com",
      "id": "string",
      "revoked_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `granted_at` | date |  |
| `granted_to_email` | string |  |
| `id` | string |  |
| `revoked_at` | date |  |

## Native endpoint

Through the native Neon API, this operation is `DELETE /projects/:project_id/permissions/:permission_id` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/revoke-permission-from-project.md) for the provider-specific parameters and requirements.

