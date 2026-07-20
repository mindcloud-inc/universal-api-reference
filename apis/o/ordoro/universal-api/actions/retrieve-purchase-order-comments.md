# Ordoro: Retrieve Purchase Order Comments

Retrieves comments for an Ordoro purchase order.

```
GET https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/retrieve-purchase-order-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ordoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/retrieve-purchase-order-comments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/retrieve-purchase-order-comments?${params}`, {
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Ordoro API, this operation is `GET /purchase_order/{po_id}/comment/` (base URL `https://api.ordoro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-purchase-order-comments.md) for the provider-specific parameters and requirements.

