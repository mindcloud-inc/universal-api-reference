# Halo Service Solutions: Create Purchase Order

Creates a new purchase order in Halo Service Solutions.

```
POST https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-purchase-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-purchase-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `[]` | array<object> | no | Purchase order payload array. |
| `[].title` | string | no | Purchase order title. |
| `[].supplier_id` | number | no | Supplier ID for the purchase order. |
| `[].client_id` | number | no | Client ID for the purchase order. |
| `[].user_id` | number | no | User ID for the purchase order. |
| `[].site_id` | number | no | Site ID for the purchase order. |
| `[].assigned_agent` | number | no | Assigned agent ID for the purchase order. |
| `[].note` | string | no | Optional note for the purchase order. |
| `[].salesorder_id` | number | no | Related sales order ID. |

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

Through the native Halo Service Solutions API, this operation is `POST /PurchaseOrder` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-purchase-order.md) for the provider-specific parameters and requirements.

