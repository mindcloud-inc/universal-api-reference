# Zydon: List Financials By Order

Retrieves financial records for an order from Zydon.

```
GET https://connect.mindcloud.co/v1/universal/zydon/latest/actions/list-financials-by-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zydon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zydon/latest/actions/list-financials-by-order?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zydon/latest/actions/list-financials-by-order?${params}`, {
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
      "id": "string",
      "order_id": "string",
      "partner_name": "Ava Chen",
      "status": "string",
      "type": "string",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Financial record identifier. |
| `order_id` | string | Order identifier associated with the financial record. |
| `partner_name` | string | Partner name associated with the financial record. |
| `status` | string | Financial record status. |
| `type` | string | Financial record type. |
| `value` | number | Financial record value. |

## Native endpoint

Through the native Zydon API, this operation is `GET /financials/order/{orderId}` (base URL `https://api.zydon.com.br/api/sales`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-financials-by-order.md) for the provider-specific parameters and requirements.

