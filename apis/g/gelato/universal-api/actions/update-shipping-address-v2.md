# Gelato: Update Shipping Address v2

Updates an order shipping address in Gelato v2.

```
PUT https://connect.mindcloud.co/v1/universal/gelato/latest/actions/update-shipping-address-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gelato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gelato/latest/actions/update-shipping-address-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderReferenceId": "string",
  "countryIsoCode": "string",
  "firstName": "Ava",
  "lastName": "Chen",
  "addressLine1": "string",
  "city": "string",
  "postcode": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gelato/latest/actions/update-shipping-address-v2', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderReferenceId": "string",
    "countryIsoCode": "string",
    "firstName": "Ava",
    "lastName": "Chen",
    "addressLine1": "string",
    "city": "string",
    "postcode": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderReferenceId` | string | yes |  |
| `countryIsoCode` | string | yes |  |
| `firstName` | string | yes |  |
| `lastName` | string | yes |  |
| `addressLine1` | string | yes |  |
| `city` | string | yes |  |
| `postcode` | string | yes |  |
| `email` | string | yes |  |
| `companyName` | string | no |  |
| `addressLine2` | string | no |  |
| `stateCode` | string | no |  |
| `phone` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Gelato API returns.

## Native endpoint

Through the native Gelato API, this operation is `PUT https://api.gelato.com/v2/order/{{orderReferenceId}}/address` (base URL `https://order.gelatoapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-shipping-address-v2.md) for the provider-specific parameters and requirements.

