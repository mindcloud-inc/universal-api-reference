# Neon: Update organization plugin configuration

Updates organization plugin configuration in Neon.

```
PUT https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-neon-auth-organization-plugin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-neon-auth-organization-plugin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string",
  "branch_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-neon-auth-organization-plugin', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `project_id` | string | yes | Neon API parameter project_id |
| `branch_id` | string | yes | Neon API parameter branch_id |
| `enabled` | boolean | no | Neon API parameter enabled |
| `organization_limit` | number | no | Neon API parameter organization_limit |
| `membership_limit` | number | no | Neon API parameter membership_limit |
| `creator_role` | list | no | Neon API parameter creator_role One of: `0`, `1`. |
| `send_invitation_email` | boolean | no | Neon API parameter send_invitation_email |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creator_role": [
        "string"
      ],
      "enabled": true,
      "membership_limit": 1,
      "organization_limit": 1,
      "send_invitation_email": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creator_role` | array |  |
| `enabled` | boolean |  |
| `membership_limit` | number |  |
| `organization_limit` | number |  |
| `send_invitation_email` | boolean |  |

## Native endpoint

Through the native Neon API, this operation is `PATCH /projects/:project_id/branches/:branch_id/auth/plugins/organization` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-neon-auth-organization-plugin.md) for the provider-specific parameters and requirements.

