# ShopWired: List product choices

Retrieves choices for a product from ShopWired.

```
GET https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/list-product-choices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShopWired `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/list-product-choices?connectionId=$CONNECTION_ID&productId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/list-product-choices?${params}`, {
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
| `productId` | number | yes | ID of the product. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "costPrice": 1,
      "customPrice": 1,
      "id": 1,
      "set": {
        "id": 1,
        "name": "Ava Chen"
      },
      "value": {
        "id": 1,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `costPrice` | number |  |
| `customPrice` | number |  |
| `id` | number |  |
| `set.id` | number |  |
| `set.name` | string |  |
| `value.id` | number |  |
| `value.name` | string |  |

## Native endpoint

Through the native ShopWired API, this operation is `GET /products/{product_id}/choices` (base URL `https://api.ecommerceapi.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-product-choices.md) for the provider-specific parameters and requirements.

