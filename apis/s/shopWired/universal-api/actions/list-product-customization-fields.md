# ShopWired: List product customisation fields

Retrieves customisation fields for a product from ShopWired.

```
GET https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/list-product-customization-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShopWired `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/list-product-customization-fields?connectionId=$CONNECTION_ID&productId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/list-product-customization-fields?${params}`, {
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
| `productId` | number | yes | ID of the product which the customisation fields are assigned to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "label": "string",
      "max_length": 1,
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `label` | string |  |
| `max_length` | number |  |
| `type` | number |  |

## Native endpoint

Through the native ShopWired API, this operation is `GET /products/{product_id}/customization-fields` (base URL `https://api.ecommerceapi.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-product-customization-fields.md) for the provider-specific parameters and requirements.

