# Neon: Send test email

Sends a test email in Neon.

```
POST https://connect.mindcloud.co/v1/universal/neon/latest/actions/send-neon-auth-test-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neon/latest/actions/send-neon-auth-test-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string",
  "branch_id": "string",
  "host": "string",
  "port": 1,
  "username": "Ava Chen",
  "password": "string",
  "sender_email": "ava@example.com",
  "sender_name": "Ava Chen",
  "recipient_email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/send-neon-auth-test-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "string",
    "branch_id": "string",
    "host": "string",
    "port": 1,
    "username": "Ava Chen",
    "password": "string",
    "sender_email": "ava@example.com",
    "sender_name": "Ava Chen",
    "recipient_email": "ava@example.com"
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
| `host` | string | yes | Neon API parameter host |
| `port` | number | yes | Neon API parameter port |
| `username` | string | yes | Neon API parameter username |
| `password` | string | yes | Neon API parameter password |
| `sender_email` | string | yes | Neon API parameter sender_email |
| `sender_name` | string | yes | Neon API parameter sender_name |
| `recipient_email` | string | yes | Neon API parameter recipient_email |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error_message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error_message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Neon API, this operation is `POST /projects/:project_id/branches/:branch_id/auth/send_test_email` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-neon-auth-test-email.md) for the provider-specific parameters and requirements.

