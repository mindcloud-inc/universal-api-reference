# Open Letter Connect: Create Order

Creates an order in Open Letter Connect.

```
POST https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Letter Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deliveryDate": "string",
  "productId": 1,
  "templateId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deliveryDate": "string",
    "productId": 1,
    "templateId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deliveryDate` | string | yes | The requested delivery date string. |
| `name` | string | no | An optional name for the order. |
| `productId` | number | yes | The product ID to order. |
| `tag` | string | no | The contact tag ID to use as the recipient source for the order. |
| `templateId` | number | yes | The template ID to use for the order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchId": "string",
      "cost": 1,
      "createdBy": "string",
      "creator": {
        "fullName": "Ava Chen",
        "id": "string"
      },
      "id": "string",
      "isLiveMode": true,
      "orgId": "string",
      "paymentStatus": "string",
      "returnContactId": "string",
      "source": "string",
      "status": "string",
      "templateUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchId` | string |  |
| `cost` | number |  |
| `createdBy` | string |  |
| `creator.fullName` | string |  |
| `creator.id` | string |  |
| `id` | string |  |
| `isLiveMode` | boolean |  |
| `orgId` | string |  |
| `paymentStatus` | string |  |
| `returnContactId` | string |  |
| `source` | string |  |
| `status` | string |  |
| `templateUrl` | string |  |

## Native endpoint

Through the native Open Letter Connect API, this operation is `POST /orders` (base URL `https://api.openletterconnect.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

