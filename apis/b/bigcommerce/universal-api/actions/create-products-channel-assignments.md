# BigCommerce: Create Products Channel Assignments



```
PUT https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/create-products-channel-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigCommerce `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/create-products-channel-assignments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "product_id": 1,
  "channel_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/create-products-channel-assignments', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "product_id": 1,
    "channel_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `product_id` | number | yes |  |
| `channel_id` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BigCommerce API returns.

## Native endpoint

Through the native BigCommerce API, this operation is `PUT /v3/catalog/products/channel-assignments` (base URL `https://api.bigcommerce.com/stores/{{credentials.storeHash}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/create-products-channel-assignments.md) for the provider-specific parameters and requirements.

