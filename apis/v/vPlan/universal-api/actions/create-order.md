# vPlan: Create Order



```
POST https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-order', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "address_id": "string",
      "code": "string",
      "collection_id": "string",
      "contact": "string",
      "created_at": "string",
      "date": "string",
      "delivered_date": "string",
      "description": "string",
      "desired_date": "string",
      "external_ref": "string",
      "external_url": "https://example.com",
      "id": "string",
      "item_id": "string",
      "meta": {},
      "note": "string",
      "project_id": "string",
      "promised_date": "string",
      "quantity": "string",
      "relation_id": "string",
      "relation_ref": "string",
      "status": "string",
      "sub_type": "string",
      "transaction": "string",
      "type": "string",
      "updated_at": "string",
      "warehouse_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address_id` | string | Address identifier. |
| `code` | string | Order code. |
| `collection_id` | string | Collection identifier. |
| `contact` | string | Order contact. |
| `created_at` | string | Creation timestamp. |
| `date` | string | Order date. |
| `delivered_date` | string | Delivered date. |
| `description` | string | Order description. |
| `desired_date` | string | Desired date. |
| `external_ref` | string | External reference. |
| `external_url` | string | External URL. |
| `id` | string | Order identifier. |
| `item_id` | string | Item identifier. |
| `meta` | object | Additional metadata. |
| `note` | string | Order note. |
| `project_id` | string | Project identifier. |
| `promised_date` | string | Promised date. |
| `quantity` | string | Order quantity. |
| `relation_id` | string | Relation identifier. |
| `relation_ref` | string | Relation reference. |
| `status` | string | Order status. |
| `sub_type` | string | Order subtype. |
| `transaction` | string | Provider transaction value. |
| `type` | string | Order type. |
| `updated_at` | string | Last update timestamp. |
| `warehouse_id` | string | Warehouse identifier. |

## Native endpoint

Through the native vPlan API, this operation is `POST /order` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

