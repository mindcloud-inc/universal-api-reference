# Chatrace: Get Contact Cart

Retrieves a contact cart from Chatrace.

```
GET https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/get-contact-cart
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatrace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/get-contact-cart?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/get-contact-cart?${params}`, {
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
      "currency": "string",
      "order_id": "string",
      "page_id": 1,
      "total": 1,
      "total_items": 1,
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `order_id` | string |  |
| `page_id` | number |  |
| `total` | number |  |
| `total_items` | number |  |
| `user_id` | number |  |

## Native endpoint

Through the native Chatrace API, this operation is `GET /contacts/:contact_id/cart` (base URL `https://api.chatrace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-cart.md) for the provider-specific parameters and requirements.

