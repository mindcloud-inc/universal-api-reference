# Paycove: Create Webhook Subscription

Creates a webhook subscription in Paycove.

```
POST https://connect.mindcloud.co/v1/universal/paycove/latest/actions/create-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/create-webhook-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetUrl": "https://example.com/paycove-webhooks",
  "event": "invoice_paid"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paycove/latest/actions/create-webhook-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetUrl": "https://example.com/paycove-webhooks",
    "event": "invoice_paid"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetUrl` | string | yes | Destination to deliver deal payload to. Example: `https://example.com/paycove-webhooks`. |
| `event` | string | yes | Webhook event type to subscribe to. Example: `invoice_paid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "destinationApp": "string",
      "event": "string",
      "id": 1,
      "notificationTemplateId": 1,
      "signingKey": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `createdAt` | date |  |
| `destinationApp` | string |  |
| `event` | string |  |
| `id` | number |  |
| `notificationTemplateId` | number |  |
| `signingKey` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Paycove API, this operation is `POST hooks` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-subscription.md) for the provider-specific parameters and requirements.

