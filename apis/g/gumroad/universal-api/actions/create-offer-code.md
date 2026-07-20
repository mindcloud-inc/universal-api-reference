# Gumroad: Create Offer Code

Creates a new offer code in Gumroad.

```
POST https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/create-offer-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gumroad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/create-offer-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "string",
  "name": "Ava Chen",
  "amountOff": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/create-offer-code', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": "string",
    "name": "Ava Chen",
    "amountOff": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | string | yes | The product ID. |
| `name` | string | yes | The coupon code used at checkout. |
| `amountOff` | number | yes | The discount amount. |
| `offerType` | string | no | Use cents or percent. |
| `maxPurchaseCount` | number | no | The maximum number of redemptions allowed. |
| `universal` | boolean | no | Whether the offer code applies to all products. |

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
        "timesUsed": 1
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
| `offerCode.timesUsed` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Gumroad API, this operation is `POST /products/:product_id/offer_codes` (base URL `https://api.gumroad.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-offer-code.md) for the provider-specific parameters and requirements.

