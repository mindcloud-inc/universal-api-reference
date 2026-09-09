# Walmart: Delete Subscription

Delete an existing webhook subscription by ID.

```
DELETE https://connect.mindcloud.co/v1/universal/walmart/latest/actions/delete-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/delete-subscription?connectionId=$CONNECTION_ID&subscriptionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriptionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/delete-subscription?${params}`, {
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
| `subscriptionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "eventType": "string",
      "eventVersion": "string",
      "message": "string",
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
| `eventType` | string |  |
| `eventVersion` | string |  |
| `message` | string |  |
| `partnerId` | string |  |
| `resourceName` | string |  |
| `status` | string |  |
| `subscribedBy` | string |  |
| `subscriptionId` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `DELETE v3/webhooks/subscriptions/:subscriptionId` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-subscription.md) for the provider-specific parameters and requirements.

