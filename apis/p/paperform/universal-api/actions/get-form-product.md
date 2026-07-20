# Paperform: Get Form Product

Retrieves a product from a Paperform form.

```
GET https://connect.mindcloud.co/v1/universal/paperform/latest/actions/get-form-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paperform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paperform/latest/actions/get-form-product?connectionId=$CONNECTION_ID&slugOrId=contact-form&productSku=SKU-123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slugOrId": "contact-form",
  "productSku": "SKU-123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paperform/latest/actions/get-form-product?${params}`, {
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
| `slugOrId` | list<string> | yes | Example: `contact-form`. |
| `productSku` | list | yes | Example: `SKU-123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "discountable": true,
      "formSlugOrId": "string",
      "images": [
        "string"
      ],
      "maximum": 1,
      "minimum": 1,
      "name": "Ava Chen",
      "price": "string",
      "quantity": 1,
      "sku": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `discountable` | boolean |  |
| `formSlugOrId` | string | Form slug or ID used to build the Paperform editor URL. |
| `images` | array<string> |  |
| `maximum` | number |  |
| `minimum` | number |  |
| `name` | string |  |
| `price` | string |  |
| `quantity` | number |  |
| `sku` | string |  |

## Native endpoint

Through the native Paperform API, this operation is `GET /forms/:slug_or_id/products/:product_sku` (base URL `https://api.paperform.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-product.md) for the provider-specific parameters and requirements.

