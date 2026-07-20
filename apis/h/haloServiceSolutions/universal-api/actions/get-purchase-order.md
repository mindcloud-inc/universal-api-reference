# Halo Service Solutions: Get Purchase Order

Retrieves a purchase order from Halo Service Solutions.

```
GET https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-purchase-order?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-purchase-order?${params}`, {
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
| `id` | number | yes | Purchase order ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigned_agent": 1,
      "client_id": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "note": "string",
      "po_ref": "string",
      "salesorder_id": 1,
      "site_id": 1,
      "status": 1,
      "supplier_id": 1,
      "supplier_name": "Ava Chen",
      "title": "string",
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
| `assigned_agent` | number |  |
| `client_id` | number |  |
| `date` | date |  |
| `id` | number | Purchase order ID |
| `note` | string |  |
| `po_ref` | string |  |
| `salesorder_id` | number |  |
| `site_id` | number |  |
| `status` | number |  |
| `supplier_id` | number |  |
| `supplier_name` | string |  |
| `title` | string |  |
| `total` | number |  |
| `user_id` | number |  |

## Native endpoint

Through the native Halo Service Solutions API, this operation is `GET /PurchaseOrder/:id` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-purchase-order.md) for the provider-specific parameters and requirements.

