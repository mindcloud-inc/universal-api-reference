# Smart Sender: List Products

Retrieves project products from Smart Sender.

```
GET https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smart Sender `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/list-products?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "category": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "essences": [
        {}
      ],
      "id": 1,
      "labels": [
        {}
      ],
      "name": "Ava Chen",
      "paymentSystems": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | object |  |
| `createdAt` | date |  |
| `essences` | array<object> |  |
| `id` | number |  |
| `labels` | array<object> |  |
| `name` | string |  |
| `paymentSystems` | array<object> |  |

## Native endpoint

Through the native Smart Sender API, this operation is `GET /v1/products` (base URL `https://api.smartsender.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

