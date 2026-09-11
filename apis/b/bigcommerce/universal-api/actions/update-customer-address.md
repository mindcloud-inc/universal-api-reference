# BigCommerce: Update Customer Address



```
PUT https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/update-customer-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigCommerce `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/update-customer-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/update-customer-address', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `first_name` | string | no |  |
| `last_name` | string | no |  |
| `company` | string | no |  |
| `address1` | string | no |  |
| `address2` | string | no |  |
| `city` | string | no |  |
| `state_or_province` | string | no |  |
| `postal_code` | string | no |  |
| `country_code` | string | no |  |
| `phone` | string | no |  |
| `address_type` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BigCommerce API returns.

## Native endpoint

Through the native BigCommerce API, this operation is `PUT /v3/customers/addresses` (base URL `https://api.bigcommerce.com/stores/{{credentials.storeHash}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/update-customer-address.md) for the provider-specific parameters and requirements.

