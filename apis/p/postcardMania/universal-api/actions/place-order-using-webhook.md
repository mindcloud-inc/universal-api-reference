# PostcardMania: Place Order using Webhook

Creates a new order in PostcardMania using a webhook.

```
POST https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/place-order-using-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostcardMania `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/place-order-using-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookID": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/place-order-using-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookID": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookID` | number | yes | Preconfigured webhook identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orderID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orderID` | number | Created order identifier. |

## Native endpoint

Through the native PostcardMania API, this operation is `POST /order/webhook/{{webhookID}}` (base URL `https://v3.pcmintegrations.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/place-order-using-webhook.md) for the provider-specific parameters and requirements.

