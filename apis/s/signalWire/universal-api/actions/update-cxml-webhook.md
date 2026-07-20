# SignalWire: Update cXML Webhook

Updates an existing cXML webhook in SignalWire.

```
PUT https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/update-cxml-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/update-cxml-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/update-cxml-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique ID of a CXML Webhook. |
| `name` | string | no | Name of the CXML Webhook. |
| `usedFor` | string | no | Used for of the CXML Webhook. |
| `primaryRequestUrl` | string | no | Primary request url of the CXML Webhook. |
| `primaryRequestMethod` | string | no | Primary request method of the CXML Webhook. |
| `fallbackRequestUrl` | string | no | Fallback request url of the CXML Webhook. |
| `fallbackRequestMethod` | string | no | Fallback request method of the CXML Webhook. |
| `statusCallbackUrl` | string | no | Status callback url of the CXML Webhook. |
| `statusCallbackMethod` | string | no | Status callback method of the CXML Webhook. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "cxml_webhook": {
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
      "display_name": "Ava Chen",
      "id": "string",
      "project_id": "string",
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
| `cxml_webhook.fallback_request_method` | string | Fallback request method of the CXML Webhook. |
| `cxml_webhook.fallback_request_url` | string | Fallback request url of the CXML Webhook. |
| `cxml_webhook.id` | string | Unique ID of the CXML Webhook. |
| `cxml_webhook.name` | string | Name of the CXML Webhook. |
| `cxml_webhook.primary_request_method` | string | Primary request method of the CXML Webhook. |
| `cxml_webhook.primary_request_url` | string | Primary request url of the CXML Webhook. |
| `cxml_webhook.status_callback_method` | string | Status callback method of the CXML Webhook. |
| `cxml_webhook.status_callback_url` | string | Status callback url of the CXML Webhook. |
| `cxml_webhook.used_for` | string | Used for of the CXML Webhook. |
| `display_name` | string | Display name of the CXMLWebhook Fabric Resource |
| `id` | string | Unique ID of the CXMLWebhook. |
| `project_id` | string | Unique ID of the Project. |
| `type` | string | Type of the Fabric Resource |
| `updated_at` | date | Date and time when the resource was updated. |

## Native endpoint

Through the native SignalWire API, this operation is `PATCH /fabric/resources/cxml_webhooks/{id}` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-cxml-webhook.md) for the provider-specific parameters and requirements.

