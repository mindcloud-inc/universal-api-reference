# Gelato: Update Shipping Address v3

Updates an order shipping address in Gelato v3.

```
PUT https://connect.mindcloud.co/v1/universal/gelato/latest/actions/update-shipping-address-v3
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gelato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gelato/latest/actions/update-shipping-address-v3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": "string",
  "country": "string",
  "firstName": "Ava",
  "lastName": "Chen",
  "addressLine1": "string",
  "city": "string",
  "postCode": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gelato/latest/actions/update-shipping-address-v3', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": "string",
    "country": "string",
    "firstName": "Ava",
    "lastName": "Chen",
    "addressLine1": "string",
    "city": "string",
    "postCode": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | string | yes |  |
| `country` | string | yes |  |
| `firstName` | string | yes |  |
| `lastName` | string | yes |  |
| `addressLine1` | string | yes |  |
| `city` | string | yes |  |
| `postCode` | string | yes |  |
| `email` | string | yes |  |
| `state` | string | no |  |
| `companyName` | string | no |  |
| `addressLine2` | string | no |  |
| `phone` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Gelato API returns.

## Native endpoint

Through the native Gelato API, this operation is `PUT /v3/orders/{{orderId}}/shipping-address` (base URL `https://order.gelatoapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-shipping-address-v3.md) for the provider-specific parameters and requirements.

