# Yampi: List Customer Carts

Retrieves abandoned carts for a customer in Yampi.

```
GET https://connect.mindcloud.co/v1/universal/yampi/latest/actions/list-customer-carts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yampi `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yampi/latest/actions/list-customer-carts?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yampi/latest/actions/list-customer-carts?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "status": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `status` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Yampi API, this operation is `GET /:merchantAlias/customers/:id/carts` (base URL `https://api.dooki.com.br/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customer-carts.md) for the provider-specific parameters and requirements.

