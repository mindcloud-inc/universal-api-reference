# BigCommerce: List Customer Addresses



```
GET https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/list-customer-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigCommerce `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/list-customer-addresses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/list-customer-addresses?${params}`, {
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
| `customer_id:in` | string | no | Filter by the ID of the customer. Also accepts comma-separated IDs to filter for multiple customers. customer_id:in=23,24,55 Accepts multiple values in one string. |
| `id:in` | string | no | Accepts multiple values as an array. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BigCommerce API returns.

## Native endpoint

Through the native BigCommerce API, this operation is `GET /v3/customers/addresses` (base URL `https://api.bigcommerce.com/stores/{{credentials.storeHash}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customer-addresses.md) for the provider-specific parameters and requirements.

