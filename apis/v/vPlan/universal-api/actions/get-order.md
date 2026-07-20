# vPlan: Get Order



```
GET https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-order?connectionId=$CONNECTION_ID&id=9b2872a9-8aac-451d-b640-be6854fb49dc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "9b2872a9-8aac-451d-b640-be6854fb49dc"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-order?${params}`, {
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
| `id` | string | yes | Order identifier. Default: `9b2872a9-8aac-451d-b640-be6854fb49dc`. |

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

Through the native vPlan API, this operation is `GET /order/[:id]` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

