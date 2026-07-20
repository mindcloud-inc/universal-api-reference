# SureCart: Create Webhook Endpoint



```
POST https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/create-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/create-webhook-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookEndpoint.url": "https://httpbin.org/post"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/create-webhook-endpoint', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookEndpoint.url": "https://httpbin.org/post"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookEndpoint.url` | string | yes | The public URL for this webhook endpoint. Example: `https://httpbin.org/post`. |
| `webhookEndpoint.description` | string | no | Optional description for the webhook endpoint. Example: `MindCloud SureCart webhook test endpoint`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "automationService": "string",
      "createdAt": 1,
      "description": "string",
      "enabled": true,
      "erroringGracePeriodEndsAt": 1,
      "erroringGracePeriodStartedAt": 1,
      "id": "string",
      "object": "string",
      "signingSecret": "string",
      "updatedAt": 1,
      "url": "https://example.com",
      "webhookEvents": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `automationService` | string |  |
| `createdAt` | number |  |
| `description` | string |  |
| `enabled` | boolean |  |
| `erroringGracePeriodEndsAt` | number |  |
| `erroringGracePeriodStartedAt` | number |  |
| `id` | string |  |
| `object` | string |  |
| `signingSecret` | string |  |
| `updatedAt` | number |  |
| `url` | string |  |
| `webhookEvents` | array<string> |  |

## Native endpoint

Through the native SureCart API, this operation is `POST v1/webhook_endpoints` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-endpoint.md) for the provider-specific parameters and requirements.

