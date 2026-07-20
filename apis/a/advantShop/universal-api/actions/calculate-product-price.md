# AdvantShop: Calculate Product Price

Calculates a product price in AdvantShop.

```
GET https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/calculate-product-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AdvantShop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/calculate-product-price?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/calculate-product-price?${params}`, {
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
| `id` | string | yes | Product identifier from AdvantShop. |
| `offerId` | number | no | Product offer identifier for price calculation. |
| `amount` | number | no | Product quantity for price calculation. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "discount": 1,
      "price": 1,
      "priceFormatted": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `discount` | number |  |
| `price` | number |  |
| `priceFormatted` | string |  |

## Native endpoint

Through the native AdvantShop API, this operation is `POST /products/{id}/price` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-product-price.md) for the provider-specific parameters and requirements.

