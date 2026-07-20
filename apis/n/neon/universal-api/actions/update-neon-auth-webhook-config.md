# Neon: Update webhook configuration for Neon Auth

Updates Neon Auth webhook configuration in Neon.

```
PUT https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-neon-auth-webhook-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-neon-auth-webhook-config" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string",
  "branch_id": "string",
  "enabled": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-neon-auth-webhook-config', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "string",
    "branch_id": "string",
    "enabled": true
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
| `enabled` | boolean | yes | Neon API parameter enabled |
| `webhook_url` | string | no | Neon API parameter webhook_url |
| `enabled_events[]` | array<list> | no | Neon API parameter enabled_events |
| `timeout_seconds` | number | no | Neon API parameter timeout_seconds |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enabled": true,
      "enabled_events": [
        [
          "string"
        ]
      ],
      "timeout_seconds": 1,
      "webhook_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabled` | boolean |  |
| `enabled_events` | array<array> |  |
| `timeout_seconds` | number |  |
| `webhook_url` | string |  |

## Native endpoint

Through the native Neon API, this operation is `PUT /projects/:project_id/branches/:branch_id/auth/webhooks` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-neon-auth-webhook-config.md) for the provider-specific parameters and requirements.

