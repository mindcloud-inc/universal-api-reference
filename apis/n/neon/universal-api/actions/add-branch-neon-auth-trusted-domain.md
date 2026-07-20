# Neon: Add domain to redirect_uri whitelist

Adds a domain to the redirect URI whitelist in Neon.

```
POST https://connect.mindcloud.co/v1/universal/neon/latest/actions/add-branch-neon-auth-trusted-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neon/latest/actions/add-branch-neon-auth-trusted-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string",
  "branch_id": "string",
  "domain": "string",
  "auth_provider": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/add-branch-neon-auth-trusted-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "string",
    "branch_id": "string",
    "domain": "string",
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
| `branch_id` | string | yes | Neon API parameter branch_id |
| `domain` | string | yes | Neon API parameter domain |
| `auth_provider` | list | yes | Neon API parameter auth_provider One of: `0`, `1`, `2`, `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Neon API, this operation is `POST /projects/:project_id/branches/:branch_id/auth/domains` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-branch-neon-auth-trusted-domain.md) for the provider-specific parameters and requirements.

