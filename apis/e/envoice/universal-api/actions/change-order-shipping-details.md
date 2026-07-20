# Envoice: Change Order Shipping Details

Updates order shipping details in Envoice.

```
PUT https://connect.mindcloud.co/v1/universal/envoice/latest/actions/change-order-shipping-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/change-order-shipping-details" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "countryId": 1,
  "email": "ava@example.com",
  "name": "Ava Chen",
  "orderId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/envoice/latest/actions/change-order-shipping-details', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "countryId": 1,
    "email": "ava@example.com",
    "name": "Ava Chen",
    "orderId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no | Shipping street address. |
| `countryId` | number | yes | Shipping country identifier. |
| `email` | string | yes | Shipping recipient email. |
| `name` | string | yes | Shipping recipient name. |
| `orderId` | number | yes | Order identifier whose shipping details should change. |
| `phoneNumber` | string | no | Shipping phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Success` | boolean | Whether order shipping details changed. |

## Native endpoint

Through the native Envoice API, this operation is `POST order/changeshippingdetails` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-order-shipping-details.md) for the provider-specific parameters and requirements.

