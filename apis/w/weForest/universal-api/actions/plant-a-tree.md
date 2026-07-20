# WeForest: Plant a tree

Creates a new tree-planting request in WeForest.

```
POST https://connect.mindcloud.co/v1/universal/weForest/latest/actions/plant-a-tree
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeForest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weForest/latest/actions/plant-a-tree" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "items[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weForest/latest/actions/plant-a-tree', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "items[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `items[]` | array<object> | yes | Array of order items with productId and quantity. |
| `sandbox` | boolean | no | Whether the order should be treated as a sandbox order. |
| `user` | object | no | End-user object for the order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customerId": 1,
      "endUser": {},
      "id": 1,
      "items": [
        {}
      ],
      "paid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `customerId` | number |  |
| `endUser` | object |  |
| `id` | number |  |
| `items` | array<object> |  |
| `paid` | boolean |  |

## Native endpoint

Through the native WeForest API, this operation is `POST /trees` (base URL `https://api.weforest.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/plant-a-tree.md) for the provider-specific parameters and requirements.

