# MoreApp: Update Webhook Subscriber

Updates a webhook subscriber in MoreApp.

```
PUT https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/update-webhook-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/update-webhook-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "209321",
  "name": "MindCloud Temp Subscriber Updated",
  "status": "ACTIVE",
  "subscriberId": "69bc494c924bd75a32934747",
  "type[]": [
    "submission.created",
    "customer.updated"
  ],
  "url": "https://example.com/moreapp-webhook-2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/update-webhook-subscriber', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "209321",
    "name": "MindCloud Temp Subscriber Updated",
    "status": "ACTIVE",
    "subscriberId": "69bc494c924bd75a32934747",
    "type[]": ["submission.created","customer.updated"],
    "url": "https://example.com/moreapp-webhook-2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes | MoreApp customer identifier. Default: `209321`. |
| `name` | string | yes | Subscriber display name. Default: `MindCloud Temp Subscriber Updated`. |
| `secret` | string | no | Optional signing secret. Default: `mindcloud-temp-secret-2`. |
| `status` | string | yes | Subscriber status. Default: `ACTIVE`. |
| `subscriberId` | string | yes | MoreApp subscriber identifier. Default: `69bc494c924bd75a32934747`. |
| `type[]` | array<string> | yes | Webhook event types. Accepts multiple values as an array. Default: `["submission.created","customer.updated"]`. |
| `url` | string | yes | Webhook URL to receive MoreApp events. Default: `https://example.com/moreapp-webhook-2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "secret": "string",
      "status": "string",
      "type": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `secret` | string |  |
| `status` | string |  |
| `type` | array<string> |  |
| `url` | string |  |

## Native endpoint

Through the native MoreApp API, this operation is `PUT /api/v1.0/webhooks/customer/{{customerId}}/subscribers/{{subscriberId}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook-subscriber.md) for the provider-specific parameters and requirements.

