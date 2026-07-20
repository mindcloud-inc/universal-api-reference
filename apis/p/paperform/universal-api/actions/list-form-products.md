# Paperform: List Form Products

Retrieves products from a Paperform form.

```
GET https://connect.mindcloud.co/v1/universal/paperform/latest/actions/list-form-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paperform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paperform/latest/actions/list-form-products?connectionId=$CONNECTION_ID&slugOrId=contact-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slugOrId": "contact-form"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paperform/latest/actions/list-form-products?${params}`, {
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
      "sku": "string",
      "sold": 1
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
| `sold` | number |  |

## Native endpoint

Through the native Paperform API, this operation is `GET /forms/:slug_or_id/products` (base URL `https://api.paperform.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-products.md) for the provider-specific parameters and requirements.

