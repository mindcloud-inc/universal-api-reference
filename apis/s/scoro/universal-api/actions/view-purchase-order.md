# Scoro: View Purchase Order

Retrieves purchase order details from Scoro.

```
GET https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-purchase-order?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-purchase-order?${params}`, {
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
| `id` | string | no | Scoro purchase order ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "modified_date": "string",
      "purchase_order_no": "string",
      "status": "string",
      "supplier_id": 1,
      "supplier_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `modified_date` | string |  |
| `purchase_order_no` | string |  |
| `status` | string |  |
| `supplier_id` | number |  |
| `supplier_name` | string |  |

## Native endpoint

Through the native Scoro API, this operation is `POST purchaseOrders/view/:id` (base URL `{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-purchase-order.md) for the provider-specific parameters and requirements.

