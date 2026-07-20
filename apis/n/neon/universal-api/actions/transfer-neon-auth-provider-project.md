# Neon: Transfer Neon-managed auth project to your own account

Transfers Neon-managed auth project to your own account in Neon.

```
POST https://connect.mindcloud.co/v1/universal/neon/latest/actions/transfer-neon-auth-provider-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neon/latest/actions/transfer-neon-auth-provider-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string",
  "auth_provider": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/transfer-neon-auth-provider-project', {
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
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string |  |

## Native endpoint

Through the native Neon API, this operation is `POST /projects/auth/transfer_ownership` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/transfer-neon-auth-provider-project.md) for the provider-specific parameters and requirements.

