# Envoice: Create Product

Creates a new product in Envoice.

```
POST https://connect.mindcloud.co/v1/universal/envoice/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "currencyId": 1,
  "items": "string",
  "name": "Ava Chen",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/envoice/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "currencyId": 1,
    "items": "string",
    "name": "Ava Chen",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `buttonCallToAction` | string | no | Product checkout button call to action. |
| `currencyId` | number | yes | Currency identifier. |
| `description` | string | no | Product description. |
| `isFeatured` | boolean | no | Whether the product is featured. |
| `items` | string | yes | JSON array of product item objects. |
| `name` | string | yes | Product name. |
| `paymentGateways` | string | no | JSON array of product payment gateway objects. |
| `shippingAmount` | number | no | Product shipping amount. |
| `shippingDescription` | string | no | Shipping description. |
| `status` | string | yes | Product availability status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ErrorMessages": [
        "string"
      ],
      "Id": 1,
      "IsFaulted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ErrorMessages` | array<string> | Error messages returned by Envoice. |
| `Id` | number | Created product identifier. |
| `IsFaulted` | boolean | Whether the request failed. |

## Native endpoint

Through the native Envoice API, this operation is `POST product/new` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

