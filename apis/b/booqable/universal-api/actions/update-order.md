# Booqable: Update Order

Updates an existing order in Booqable.

```
PUT https://connect.mindcloud.co/v1/universal/booqable/latest/actions/update-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Booqable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/booqable/latest/actions/update-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "a8867535-86ae-4958-bdda-a85f3d3c0073",
  "data": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/booqable/latest/actions/update-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "a8867535-86ae-4958-bdda-a85f3d3c0073",
    "data": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The UUID of the order to update. Example: `a8867535-86ae-4958-bdda-a85f3d3c0073`. |
| `data` | object | yes | JSON:API order payload with the nested `data` object expected by Booqable. Include the order id, type, and any attributes or relationships you want to update. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields.orders` | string | no | Comma-separated order fields to include instead of the default fields. Example: `created_at,updated_at,number`. |
| `include` | string | no | Comma-separated relationships to sideload. Example: `customer,coupon,start_location`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Order attributes object. |
| `id` | string | Order UUID. |
| `relationships` | object | Order relationships object. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Booqable API, this operation is `PUT /orders/:id` (base URL `https://mindcloud.booqable.com/api/4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-order.md) for the provider-specific parameters and requirements.

