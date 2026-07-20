# OTO: List Orders

Retrieves a list of orders from OTO.

```
GET https://connect.mindcloud.co/v1/universal/oTO/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OTO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oTO/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oTO/latest/actions/list-orders?${params}`, {
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
| `perPage` | number | no | Maximum number of orders to return per page. |
| `page` | number | no | Page number to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
      "orders": [
        {}
      ],
      "perPage": 1,
      "success": true,
      "totalCount": 1,
      "totalPage": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number |  |
| `orders` | array<object> |  |
| `perPage` | number |  |
| `success` | boolean |  |
| `totalCount` | number |  |
| `totalPage` | number |  |

## Native endpoint

Through the native OTO API, this operation is `GET /orders` (base URL `https://api.tryoto.com/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

