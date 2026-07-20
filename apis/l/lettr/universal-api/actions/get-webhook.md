# Lettr: Get Webhook



```
GET https://connect.mindcloud.co/v1/universal/lettr/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lettr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lettr/latest/actions/get-webhook?connectionId=$CONNECTION_ID&webhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lettr/latest/actions/get-webhook?${params}`, {
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
| `webhookId` | string | yes | Webhook identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "auth_type": "string",
        "enabled": true,
        "event_types": [
          "string"
        ],
        "has_auth_credentials": true,
        "id": "string",
        "last_failure_at": "string",
        "last_status": "string",
        "last_successful_at": "string",
        "name": "Ava Chen",
        "url": "https://example.com"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Webhook payload. |
| `data.auth_type` | string | Webhook authentication type. |
| `data.enabled` | boolean | Whether the webhook is enabled. |
| `data.event_types` | array<string> | Subscribed event types. |
| `data.has_auth_credentials` | boolean | Whether auth credentials are stored. |
| `data.id` | string | Webhook ID. |
| `data.last_failure_at` | string | Last failed delivery timestamp when present. |
| `data.last_status` | string | Last delivery status when present. |
| `data.last_successful_at` | string | Last successful delivery timestamp when present. |
| `data.name` | string | Webhook name. |
| `data.url` | string | Webhook target URL. |
| `message` | string | Webhook retrieval status message. |

## Native endpoint

Through the native Lettr API, this operation is `GET /webhooks/:webhookId` (base URL `https://app.lettr.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

