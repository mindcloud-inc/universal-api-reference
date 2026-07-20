# Paycove: Delete Product

Deletes a product from Paycove.

```
DELETE https://connect.mindcloud.co/v1/universal/paycove/latest/actions/delete-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/delete-product?connectionId=$CONNECTION_ID&productId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paycove/latest/actions/delete-product?${params}`, {
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
| `productId` | string | yes | Product ID. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "successMsg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `successMsg` | string |  |

## Native endpoint

Through the native Paycove API, this operation is `DELETE products/:product_id` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-product.md) for the provider-specific parameters and requirements.

