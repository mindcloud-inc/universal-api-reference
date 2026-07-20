# Gumroad: List Offer Codes

Retrieves offer codes for a Gumroad product.

```
GET https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/list-offer-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gumroad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/list-offer-codes?connectionId=$CONNECTION_ID&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/list-offer-codes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | string | yes | The product ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "offerCodes": [
        [
          {}
        ]
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `offerCodes[]` | array<object> |  |
| `offerCodes[].amountCents` | number |  |
| `offerCodes[].id` | string |  |
| `offerCodes[].maxPurchaseCount` | number |  |
| `offerCodes[].name` | string |  |
| `offerCodes[].percentOff` | number |  |
| `offerCodes[].timesUsed` | number |  |
| `offerCodes[].universal` | boolean |  |
| `success` | boolean |  |

## Native endpoint

Through the native Gumroad API, this operation is `GET /products/:product_id/offer_codes` (base URL `https://api.gumroad.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-offer-codes.md) for the provider-specific parameters and requirements.

