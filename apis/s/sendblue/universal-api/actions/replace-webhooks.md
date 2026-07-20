# Sendblue: Replace Webhooks

Replaces webhooks in Sendblue.

```
PUT https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/replace-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendblue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/replace-webhooks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/replace-webhooks', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `receiveWebhooks[]` | array<string> | no | Webhook URLs for inbound receive events. Accepts multiple values as an array. |
| `outboundWebhooks[]` | array<string> | no | Webhook URLs for outbound status events. Accepts multiple values as an array. |
| `typingIndicatorWebhooks[]` | array<string> | no | Webhook URLs for typing indicator events. Accepts multiple values as an array. |
| `callLogWebhooks[]` | array<string> | no | Webhook URLs for call log events. Accepts multiple values as an array. |
| `contactCreatedWebhooks[]` | array<string> | no | Webhook URLs for contact-created events. Accepts multiple values as an array. |
| `lineAssignedWebhooks[]` | array<string> | no | Webhook URLs for line-assigned events. Accepts multiple values as an array. |
| `lineBlockedWebhooks[]` | array<string> | no | Webhook URLs for line-blocked events. Accepts multiple values as an array. |
| `globalSecret` | string | no | Global secret applied to all webhook deliveries. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string",
      "webhooks": {
        "receive": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | string |  |
| `webhooks.receive[]` | string |  |

## Native endpoint

Through the native Sendblue API, this operation is `PUT /api/account/webhooks` (base URL `https://api.sendblue.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-webhooks.md) for the provider-specific parameters and requirements.

