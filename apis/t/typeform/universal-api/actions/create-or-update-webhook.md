# Typeform: Create or Update Webhook



```
PUT https://connect.mindcloud.co/v1/universal/typeform/latest/actions/create-or-update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/typeform/latest/actions/create-or-update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "tag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typeform/latest/actions/create-or-update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "tag": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `enabled` | boolean | no | Whether webhook delivery is enabled. |
| `eventTypes` | object | no | Webhook event types configuration. |
| `formId` | string | yes | Typeform form identifier. |
| `secret` | string | no | Webhook signing secret. |
| `tag` | string | yes | Webhook tag. |
| `url` | string | no | Destination URL for webhook deliveries. |
| `verifySsl` | boolean | no | Whether SSL certificate verification is enabled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "eventTypes": {
        "formResponse": true
      },
      "formId": "string",
      "id": "string",
      "secret": "string",
      "tag": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "verifySsl": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `enabled` | boolean | Whether webhook is enabled. |
| `eventTypes` | object | Webhook event type configuration. |
| `eventTypes.formResponse` | boolean | Whether form_response events are enabled. |
| `formId` | string | Form ID. |
| `id` | string | Webhook ID. |
| `secret` | string | Webhook secret. |
| `tag` | string | Webhook tag. |
| `updatedAt` | date | Last update timestamp. |
| `url` | string | Webhook destination URL. |
| `verifySsl` | boolean | Whether SSL verification is enabled. |

## Native endpoint

Through the native Typeform API, this operation is `PUT /forms/:formId/webhooks/:tag` (base URL `https://api.typeform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-webhook.md) for the provider-specific parameters and requirements.

