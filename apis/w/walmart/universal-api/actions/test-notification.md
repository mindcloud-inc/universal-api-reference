# Walmart: Test Notification

Send a test notification to a destination URL using a sample payload.

```
POST https://connect.mindcloud.co/v1/universal/walmart/latest/actions/test-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/test-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/walmart/latest/actions/test-notification', {
  method: 'POST',
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
| `eventType` | list<string> | no | Filter results to a specific event type. Refer to the events section for the list of available event types. |
| `resourceName` | list<string> | no | Filter results to a specific resource (functional category) that the event type maps to. Refer to the events section for the list of available resource names. |
| `eventUrl` | string | no | Destination URL where notifications are delivered. |
| `eventVersion` | string | no | Default: `V1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelType": "string",
      "eventType": "string",
      "eventUrl": "https://example.com",
      "eventVersion": "string",
      "partnerId": "string",
      "resourceName": "Ava Chen",
      "status": "string",
      "subscribedBy": "string",
      "subscriptionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelType` | string |  |
| `eventType` | string |  |
| `eventUrl` | string |  |
| `eventVersion` | string |  |
| `partnerId` | string |  |
| `resourceName` | string |  |
| `status` | string |  |
| `subscribedBy` | string |  |
| `subscriptionId` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `POST /v3/webhooks/test` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-notification.md) for the provider-specific parameters and requirements.

