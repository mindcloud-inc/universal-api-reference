# PIMMS: Track Sale

Creates a new tracked sale event in PIMMS.

```
POST https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/track-sale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PIMMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/track-sale" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "paymentProcessor": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/track-sale', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "paymentProcessor": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalId` | string | no | This is the unique identifier for the customer in the client's app. This is used to track the customer's journey. |
| `amount` | number | yes | The amount of the sale. Should be passed in cents. |
| `paymentProcessor` | string | yes | The payment processor via which the sale was made. |
| `eventName` | string | no | The name of the sale event. It can be used to track different types of event for example 'Purchase', 'Upgrade', 'Payment', etc. |
| `invoiceId` | string | no | The invoice ID of the sale. |
| `currency` | string | no | The currency of the sale. Accepts ISO 4217 currency codes. |
| `metadata` | object | no | Additional metadata to be stored with the sale event. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customer": {},
      "eventName": "Ava Chen",
      "sale": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer` | object |  |
| `eventName` | string |  |
| `sale` | object |  |

## Native endpoint

Through the native PIMMS API, this operation is `POST /track/sale` (base URL `https://api.pimms.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-sale.md) for the provider-specific parameters and requirements.

