# BaseLinker: Set Order Fields

Updates order fields in BaseLinker.

```
PUT https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/set-order-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BaseLinker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/set-order-fields" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "order_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/set-order-fields', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "order_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `order_id` | number | yes | Order identifier from the BaseLinker order manager. |
| `user_comments` | string | no | Customer-visible order comments. |
| `admin_comments` | string | no | Internal admin comments for the order. |
| `email` | string | no | Customer email address. |
| `phone` | string | no | Customer phone number. |
| `delivery_method` | string | no | Delivery method name visible on the order. |
| `delivery_price` | number | no | Delivery price value. |
| `pick_state` | boolean | no | Picking state flag. |
| `pack_state` | boolean | no | Packing state flag. |
| `star` | number | no | Star marker value from 0 to 3. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parameters` | object | no | Optional raw BaseLinker parameters merged with the typed fields before request serialization. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | SUCCESS when the order fields were updated. |

## Native endpoint

Through the native BaseLinker API, this operation is `POST /connector.php` (base URL `https://api.baselinker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-order-fields.md) for the provider-specific parameters and requirements.

