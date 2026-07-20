# Gelato: Price

Retrieves product prices from Gelato by country and currency.

```
GET https://connect.mindcloud.co/v1/universal/gelato/latest/actions/price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gelato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gelato/latest/actions/price?connectionId=$CONNECTION_ID&productUid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productUid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gelato/latest/actions/price?${params}`, {
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
| `productUid` | string | yes |  |
| `country` | string | no |  |
| `currency` | string | no |  |
| `pageCount` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "currency": "string",
      "pageCount": 1,
      "price": 1,
      "productUid": "string",
      "quantity": 1,
      "shipmentPrice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string | Country code for the price row. |
| `currency` | string | Currency code for the price row. |
| `pageCount` | number | Page count for the price tier. |
| `price` | number | Product price. |
| `productUid` | string | Gelato product identifier. |
| `quantity` | number | Quantity for the price tier. |
| `shipmentPrice` | number | Shipment price. |

## Native endpoint

Through the native Gelato API, this operation is `GET https://product.gelatoapis.com/v3/products/{{productUid}}/prices` (base URL `https://order.gelatoapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/price.md) for the provider-specific parameters and requirements.

