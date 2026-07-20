# Chatrace: Get Contact Order

Retrieves an order from a Chatrace contact.

```
GET https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/get-contact-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatrace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/get-contact-order?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/get-contact-order?${params}`, {
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
      "created_at": "string",
      "currency": "string",
      "id": "string",
      "page_id": 1,
      "status": "string",
      "total": 1,
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `currency` | string |  |
| `id` | string |  |
| `page_id` | number |  |
| `status` | string |  |
| `total` | number |  |
| `user_id` | number |  |

## Native endpoint

Through the native Chatrace API, this operation is `GET /contacts/:contact_id/order/:order_id` (base URL `https://api.chatrace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-order.md) for the provider-specific parameters and requirements.

