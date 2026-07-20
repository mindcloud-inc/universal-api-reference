# BaseLinker: Update Inventory Products Stock

Updates inventory product stock in BaseLinker.

```
PUT https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/update-inventory-products-stock
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BaseLinker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/update-inventory-products-stock" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inventory_id": 1,
  "products": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/update-inventory-products-stock', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inventory_id": 1,
    "products": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inventory_id` | number | yes | Inventory identifier. |
| `products` | object | yes | Stock update payload keyed by product and warehouse identifiers. |

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
      "counter": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `counter` | number |  |
| `status` | string |  |

## Native endpoint

Through the native BaseLinker API, this operation is `POST /connector.php` (base URL `https://api.baselinker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-inventory-products-stock.md) for the provider-specific parameters and requirements.

