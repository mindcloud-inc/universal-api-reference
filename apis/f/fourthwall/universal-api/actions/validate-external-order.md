# Fourthwall: Validate External Order

Validates an external order in Fourthwall before creation.

```
POST https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/validate-external-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fourthwall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/validate-external-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "items[]": [
    {}
  ],
  "shippingAddress": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/validate-external-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "items[]": [{}],
    "shippingAddress": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `items[]` | array<object> | yes | Array of external order items to validate. Each item requires offerId, variantId, and quantity. |
| `shippingAddress` | object | yes | Shipping address object. Required fields: firstName, lastName, address1, city, zip, and country. address2, state, and phone are optional. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {
          "code": "string",
          "field": "string",
          "message": "string"
        }
      ],
      "estimatedCosts": {
        "fulfillmentFee": {
          "currency": "string",
          "value": 1
        },
        "manufacturingCost": {
          "currency": "string",
          "value": 1
        },
        "shippingCost": {
          "currency": "string",
          "value": 1
        },
        "totalCreatorCost": {
          "currency": "string",
          "value": 1
        }
      },
      "estimatedDelivery": {
        "maxDate": "2026-05-07T12:00:00.000Z",
        "minDate": "2026-05-07T12:00:00.000Z"
      },
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors[].code` | string |  |
| `errors[].field` | string |  |
| `errors[].message` | string |  |
| `estimatedCosts.fulfillmentFee.currency` | string |  |
| `estimatedCosts.fulfillmentFee.value` | number |  |
| `estimatedCosts.manufacturingCost.currency` | string |  |
| `estimatedCosts.manufacturingCost.value` | number |  |
| `estimatedCosts.shippingCost.currency` | string |  |
| `estimatedCosts.shippingCost.value` | number |  |
| `estimatedCosts.totalCreatorCost.currency` | string |  |
| `estimatedCosts.totalCreatorCost.value` | number |  |
| `estimatedDelivery.maxDate` | date |  |
| `estimatedDelivery.minDate` | date |  |
| `valid` | boolean |  |

## Native endpoint

Through the native Fourthwall API, this operation is `POST /open-api/v1.0/external-orders/validate` (base URL `https://api.fourthwall.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-external-order.md) for the provider-specific parameters and requirements.

