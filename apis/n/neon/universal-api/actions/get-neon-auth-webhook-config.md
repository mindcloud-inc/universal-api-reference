# Neon: Get webhook configuration for Neon Auth

Retrieves Neon Auth webhook configuration from Neon.

```
GET https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-neon-auth-webhook-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-neon-auth-webhook-config?connectionId=$CONNECTION_ID&project_id=string&branch_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string",
  "branch_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-neon-auth-webhook-config?${params}`, {
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

Through the native Neon API, this operation is `GET /projects/:project_id/branches/:branch_id/auth/webhooks` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-neon-auth-webhook-config.md) for the provider-specific parameters and requirements.

