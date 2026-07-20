# Gumroad: Update Offer Code

Updates an existing offer code in Gumroad.

```
PUT https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/update-offer-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gumroad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/update-offer-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/update-offer-code', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | string | yes | The product ID. |
| `id` | string | yes | The offer code ID. |
| `offerCode` | string | no | The offer code name. |
| `maxPurchaseCount` | number | no | The maximum number of redemptions allowed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "offerCode": {
        "amountCents": 1,
        "id": "string",
        "maxPurchaseCount": 1,
        "name": "Ava Chen",
        "universal": true
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `offerCode` | object |  |
| `offerCode.amountCents` | number |  |
| `offerCode.id` | string |  |
| `offerCode.maxPurchaseCount` | number |  |
| `offerCode.name` | string |  |
| `offerCode.universal` | boolean |  |
| `success` | boolean |  |

## Native endpoint

Through the native Gumroad API, this operation is `PUT /products/:product_id/offer_codes/:id` (base URL `https://api.gumroad.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-offer-code.md) for the provider-specific parameters and requirements.

