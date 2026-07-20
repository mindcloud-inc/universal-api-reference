# SignalWire: Create SWML Webhook

Creates a new SWML webhook in SignalWire.

```
POST https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-swml-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-swml-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "primaryRequestUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-swml-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "primaryRequestUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Name of the SWML Webhook. |
| `usedFor` | string | no | Used for of the SWML Webhook. |
| `primaryRequestUrl` | string | yes | Primary request url of the SWML Webhook. |
| `primaryRequestMethod` | string | no | Primary request method of the SWML Webhook. |
| `fallbackRequestUrl` | string | no | Fallback request url of the SWML Webhook. |
| `fallbackRequestMethod` | string | no | Fallback request method of the SWML Webhook. |
| `statusCallbackUrl` | string | no | Status callback url of the SWML Webhook. |
| `statusCallbackMethod` | string | no | Status callback method of the SWML Webhook. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "display_name": "Ava Chen",
      "id": "string",
      "project_id": "string",
      "swml_webhook": {
        "fallback_request_method": "string",
        "fallback_request_url": "https://example.com",
        "id": "string",
        "name": "Ava Chen",
        "primary_request_method": "string",
        "primary_request_url": "https://example.com",
        "status_callback_method": "string",
        "status_callback_url": "https://example.com",
        "used_for": "string"
      },
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Date and time when the resource was created. |
| `display_name` | string | Display name of the SWML Webhook Fabric Resource |
| `id` | string | Unique ID of the SWML Webhook. |
| `project_id` | string | Unique ID of the Project. |
| `swml_webhook.fallback_request_method` | string | Fallback request method of the SWML Webhook. |
| `swml_webhook.fallback_request_url` | string | Fallback request url of the SWML Webhook. |
| `swml_webhook.id` | string | Unique ID of the SWML Webhook. |
| `swml_webhook.name` | string | Name of the SWML Webhook. |
| `swml_webhook.primary_request_method` | string | Primary request method of the SWML Webhook. |
| `swml_webhook.primary_request_url` | string | Primary request url of the SWML Webhook. |
| `swml_webhook.status_callback_method` | string | Status callback method of the SWML Webhook. |
| `swml_webhook.status_callback_url` | string | Status callback url of the SWML Webhook. |
| `swml_webhook.used_for` | string | Used for of the SWML Webhook. |
| `type` | string | Type of the Fabric Resource |
| `updated_at` | date | Date and time when the resource was updated. |

## Native endpoint

Through the native SignalWire API, this operation is `POST /fabric/resources/swml_webhooks` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-swml-webhook.md) for the provider-specific parameters and requirements.

