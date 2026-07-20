# Yampi: List Order Addresses

Retrieves the addresses for an order in Yampi.

```
GET https://connect.mindcloud.co/v1/universal/yampi/latest/actions/list-order-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yampi `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yampi/latest/actions/list-order-addresses?connectionId=$CONNECTION_ID&limit=25&offset=0&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yampi/latest/actions/list-order-addresses?${params}`, {
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
| `orderId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "id": 1,
      "state": "string",
      "street": "string",
      "zipcode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `id` | number |  |
| `state` | string |  |
| `street` | string |  |
| `zipcode` | string |  |

## Native endpoint

Through the native Yampi API, this operation is `GET /:merchantAlias/orders/:orderId/addresses` (base URL `https://api.dooki.com.br/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-order-addresses.md) for the provider-specific parameters and requirements.

