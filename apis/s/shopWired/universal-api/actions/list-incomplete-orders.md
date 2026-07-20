# ShopWired: List incomplete orders

Retrieves incomplete orders from ShopWired.

```
GET https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/list-incomplete-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShopWired `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/list-incomplete-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/list-incomplete-orders?${params}`, {
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
| `from` | string | no | Return orders created after this UNIX timestamp. |

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
      "paymentMethod": "string",
      "reference": 1,
      "subTotal": 1,
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
| `paymentMethod` | string |  |
| `reference` | number |  |
| `subTotal` | number |  |
| `total` | number |  |

## Native endpoint

Through the native ShopWired API, this operation is `GET /incomplete-orders` (base URL `https://api.ecommerceapi.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-incomplete-orders.md) for the provider-specific parameters and requirements.

