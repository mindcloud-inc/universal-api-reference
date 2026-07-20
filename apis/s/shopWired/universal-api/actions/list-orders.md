# ShopWired: List orders

Retrieves orders from ShopWired.

```
GET https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShopWired `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/list-orders?${params}`, {
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
| `ids` | list<number> | no | Comma-separated list of specific order IDs to return, maximum 50. Accepts multiple values in one string, delimited by `,`. |
| `archived` | number | no | Specify 0 for non-archived orders, 1 for archived orders. |
| `status` | number | no | The ID of the order status. |
| `from` | string | no | Return orders created after this UNIX timestamp. |
| `to` | string | no | Return orders created before this UNIX timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "billingAddress": {
        "emailAddress": "ava@example.com"
      },
      "created": "string",
      "id": 1,
      "reference": 1,
      "status": {
        "id": 1,
        "name": "Ava Chen"
      },
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `billingAddress.emailAddress` | string |  |
| `created` | string |  |
| `id` | number |  |
| `reference` | number |  |
| `status.id` | number |  |
| `status.name` | string |  |
| `total` | number |  |

## Native endpoint

Through the native ShopWired API, this operation is `GET /orders` (base URL `https://api.ecommerceapi.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

