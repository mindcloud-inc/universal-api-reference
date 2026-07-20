# Gumroad: Get Offer Code

Retrieves an offer code from Gumroad.

```
GET https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/get-offer-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gumroad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/get-offer-code?connectionId=$CONNECTION_ID&productId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/get-offer-code?${params}`, {
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
| `id` | string | yes | The offer code ID. |

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

Through the native Gumroad API, this operation is `GET /products/:product_id/offer_codes/:id` (base URL `https://api.gumroad.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-offer-code.md) for the provider-specific parameters and requirements.

