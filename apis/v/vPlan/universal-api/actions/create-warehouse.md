# vPlan: Create Warehouse



```
POST https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-warehouse
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-warehouse" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-warehouse', {
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
      "code": "string",
      "created_at": "string",
      "external_ref": "string",
      "id": "string",
      "name": "Ava Chen",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Warehouse code. |
| `created_at` | string | Creation timestamp. |
| `external_ref` | string | External reference. |
| `id` | string | Warehouse identifier. |
| `name` | string | Warehouse name. |
| `updated_at` | string | Last update timestamp. |

## Native endpoint

Through the native vPlan API, this operation is `POST /warehouse` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-warehouse.md) for the provider-specific parameters and requirements.

