# Chatrace: Remove Product From Cart

Removes a product from a Chatrace contact cart.

```
DELETE https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/remove-product-from-cart
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatrace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/remove-product-from-cart?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/remove-product-from-cart?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Chatrace API, this operation is `DELETE /contacts/:contact_id/cart/:product_id` (base URL `https://api.chatrace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-product-from-cart.md) for the provider-specific parameters and requirements.

