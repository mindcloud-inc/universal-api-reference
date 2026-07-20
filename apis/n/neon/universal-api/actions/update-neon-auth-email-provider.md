# Neon: Update email provider configuration

Updates email provider configuration in Neon.

```
PUT https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-neon-auth-email-provider
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-neon-auth-email-provider" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string",
  "branch_id": "string",
  "requestBody": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-neon-auth-email-provider', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "string",
    "branch_id": "string",
    "requestBody": {}
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
| `requestBody` | object | yes | Neon API parameter requestBody |

## Response

```json
{
  "success": true,
  "data": [
    {
      "host": "string",
      "password": "string",
      "port": 1,
      "sender_email": "ava@example.com",
      "sender_name": "Ava Chen",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `host` | string |  |
| `password` | string |  |
| `port` | number |  |
| `sender_email` | string |  |
| `sender_name` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Neon API, this operation is `PATCH /projects/:project_id/branches/:branch_id/auth/email_provider` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-neon-auth-email-provider.md) for the provider-specific parameters and requirements.

